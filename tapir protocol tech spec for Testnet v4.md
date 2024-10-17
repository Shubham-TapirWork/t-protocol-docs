# tapir protocol tech spec for Testnet v4


- [LRT module](#LRT%20module)
	- [Competition with the same functionality](#Competition%20with%20the%20same%20functionality)
	- [Functionality](#Functionality)
		- [User actions](#User%20actions)
	- [Components](#Components)
	- [Testnet reqeirements](#Testnet%20reqeirements)
- [Depeg protection module](#Depeg%20protection%20module)
	- [Functionality](#Functionality)
		- [User actions](#User%20actions)
		- [User journey](#User%20journey)
	- [Components](#Components)
	- [Lifecycle](#Lifecycle)
		- [Depeg module](#Depeg%20module)
		- [Depeg pools](#Depeg%20pools)
			- [Initiation](#Initiation)
			- [Active pool interaction](#Active%20pool%20interaction)
			- [Depeg resolution](#Depeg%20resolution)
			- [Funds redemption](#Funds%20redemption)
	- [Testnet reqeirements](#Testnet%20reqeirements)
- [AMM pool for Depeg module](#AMM%20pool%20for%20Depeg%20module)
	- [Functionality](#Functionality)
		- [User actions](#User%20actions)
	- [Testnet reqeirements](#Testnet%20reqeirements)
- [Fixed yield module](#Fixed%20yield%20module)
	- [Functionality](#Functionality)
		- [User actions](#User%20actions)
		- [User journey](#User%20journey)
	- [Components](#Components)
	- [Lifecycle](#Lifecycle)
		- [Fixed yield module](#Fixed%20yield%20module)
		- [Fixed Yield pools](#Fixed%20Yield%20pools)
			- [Initiation](#Initiation)
			- [Active pool interaction](#Active%20pool%20interaction)
			- [Yield resolution](#Yield%20resolution)
			- [Funds redemption](#Funds%20redemption)



## LRT module 
This is a module that pools funds from restaker and mints LRTs in their stead. It then allocates the funds to strategies, which in our case will be deployment in different restaking networks. This module is similar to what competition offers.

### Competition with the same functionality 

(any LST / LRT protocol with rebasing + wrapped token)

lido.fi 
ether.fi


### Functionality 

#### User actions

- Depositing 
    - Deposit ETH (receive tETH)
    - can withdraw ETH(send tETH
- Wrapping 
    - wrap tETH into wtETH(send tETH)
    - unwrap wtETH into tETH(send wtETH)

### Components 

- **beacon oracle** reporting beacon chain balance to the smart contract 
- **pooling logic** responsible for user interactions & minting & burning of tETH+wtETH 



### Testnet reqeirements 

- pooling smart contract logic
- mock oracle is enough 


## Depeg protection module
This module allows for splitting 1 wtETH into two tokens, 0.5DP_ wtETH and 0.5YB_ wtETH. One of which carries all the depeg risk of wtETH. 

### Functionality 

- Factory contract 
    - here manager can deploing DP_ wtETH & YB_ wtETH ERC20 for every epoch
        - e.g. epoch ending in June 2024 would have tokens DP_ wtETH_0624 & YB_ wtETH_0624
- Redemption mechanism 
    - redeems DP_ wtETH & YB_ wtETH for underlying 
        - logic determining redemption before & after expiry 

#### User actions

- Depositing 
    - Deposit wtETH (receive 0.5DP_ wtETH and 0.5YB_ wtETH)
    - can withdraw wtETH(send 0.5DP_ wtETH and 0.5YB_ wtETH)
- Redeeming 
    - wrap tETH into wtETH(send tETH)
    - unwrap wtETH into tETH(send wtETH)


#### User journey

see example in litepaper [[t-protocol-docs/Tapir protocol litepaper v1.1#Example]]

### Components 

- **token splitting logic**
- **token redemption logic**
    - **depeg resolver** - logic resolving if there had been a depeg event and its size 



### Lifecycle 

#### Depeg module 
Depeg module can be thought of a factory smart contract that creates Depeg pool instances, each instace defined by the time period of its creation. 

**Example**
To give a practical example, a depeg pool could be created for 90 day duration and manager would create a pool 6 times per year, so that the whole year is covered with overlaps to allow for users having uninterrupted depeg coverage.


#### Depeg pools 


##### Initiation 
At this stage Depeg module manager initializes a pool by calling the function below on the Depeg module contract. He needs to define the pool duration `_poolActiveDuration` (e.g. active for 90 days).

the function description would look something like this: 
```solidity
function initDepegPool(_poolActiveDuration) public onlyManager
```

This function will create 3 new contracts instaces, each name labelled with `241010`
- depeg pool instance `241010` contract (instances are labeled based on the day & month & year they have been created in in `YYMMDD` format, *Notice:* two pool instances should not be created in the single day to avoid confusion in naming of ERC20s)
- DP ERC20 instance `241010` contract
- YB ERC20 instance `241010` contract 

At creation of a depeg pool these variables are set:
`initSharePrice = currentSharePrice()` defines the initial share price of wtETH at pool creation, this will be used to determine if depeg took place during the lifetime of the pool instance
`initializedAtBlock = current.block` defines at which block is the pool initialize
`deactivateAtBlock = current.block + _poolActiveDuration` defines at which block the pool becomes active 
`poolIsActive = True` this sets the pool to be active at the initialisation
`DepegResolved = false` this sets the depeg resolver to false at initialisation
`poolIsDepegged = false` this resolves if depeg happened
`depegSize = 0` this defines the depeg size in percentages times 10^18, e.g. 10% depeg, will translate into 0.1x10^18
##### Active pool interaction
Once the pool has been initiated, users can start interacting with the pool to split their `wtETH` into `DP_wtETH_241010` and `YB_wtETH_241010` or reverse the process.

```solidity

// for splitting 
function splitToken(_amount_of_wtETH) public {
    require(checkPoolIsActive())
    // 1. transfers wtETH from user
    // 2. mints DP_wtETH_241010 for the user in the amount 0.5*_amount_of_wtETH
    //    mints YB_wtETH_241010 for the user in the amount 0.5*_amount_of_wtETH
}

// for recombining split tokens 
function unSplitToken(_amount_of_wtETH_to_unsplit) public {
    require(checkPoolIsActive())
    // 1. transfers DP_wtETH_241010 and YB_wtETH_241010 from user in equal amounts _amount_of_wtETH_to_unsplit
    // 2. burns DP_wtETH_241010 for the user in the amount _amount_of_wtETH_to_unsplit
    //    burns YB_wtETH_241010 for the user in the amount _amount_of_wtETH_to_unsplit
    // 3. transfers wtETH to the user in 2*_amount_of_wtETH_to_unsplit
}

// checks if pool is in active state
function checkPoolIsActive() public returns(bool) {
    if(current.block > deactivateAtBlock) {
    poolIsActive = false;
    }
    return poolIsActive; 
}


```

##### Depeg resolution


Once the `deactivateAtBlock` block has been reached the pool is ready for redemptions. Redemption phase of the smart contract is can start once  `poolIsActive` is set to `false`.  The change of this variable is achieved by triggering any function, most directly by calling `checkPoolIsActive()`.


Once pool is no longer active, it needs to be resolved if depeg happened and what is its magnitude. This is done by calling `resolvePriceDepeg()` which upon successful call will switch  `DepegResolved`  to `True`.  
If depeg happened `poolIsDepegged` will change to `True` value and the `depegSize` value will be set. This variable tells the pool at what price should the `DP` and `YB` assets be redeemed at. 

[!Note]
[@giorgi let's think of a best way to assure this]
> The function call `resolvePriceDepeg()` is time sensitive and should be called right after the pool is deactivated. This is because it defines the size of depeg `depegSize` (in case depeg took place), which is time sensitive and will increased with passed time. 
> ?? can we try to update the pool state and resolve price depeg at every `sharePrice` update?  




```solidity

bool DepegResolved; 
bool poolIsDepegged;
uint256 depegSize;

// checks current share price against the one at the beginning of the depeg pool
function resolvePriceDepeg() public {
    require(!checkPoolIsActive(), "the pool is still active")
    require(!DepegResolved, "the depeg is already resolved")
    if(initSharePrice > currentSharePrice()){
        poolIsDepegged = True
        depegSize = 10^18 - currentSharePrice() * 10^18 / initSharePrice // at 10% depeg should resolve into 0.1 * 10**18, this means that current share price is 10% lower than at the pool initialisation
        }     
    DepegResolved = True;

}


```


##### Funds redemption
Now users can redeem their `YB` and `DP` assets. They need to approve both ERC20s and call the function below.

```solidity

function redeemTokens(_amountYB, _amountPT) public {
    require(DepegResolved, "the depeg is not resolved");
    
    // 1. burns DP_wtETH_241010 and YB_wtETH_241010 from user's address in appropriate amounts specified in the input -> _amountYB, _amountDP
    // 2. calculates how much _amountWtETHtoSend to send for DP_wtETH_241010 and YB_wtETH_241010
    _amountWtETHtoSend = 0
    if(poolIsDepegged = false) {
    _amountWtETHtoSend = _amountYB + _amountDP}
    if(poolIsDepegged = True) {
    _amountWtETHtoSend = _amountDP + _amountDP*depegSize + _amountYB - _amountYB*depegSize) // TODO double check if this is correct
    // 3. send wtETH to the user 

}


```



### Testnet reqeirements 

- full functionality of this module is required 


## AMM pool for Depeg module
For every DP_ wtETH / YB_ wtETH in every period a pool needs to be deployed that allows for trading of these two assets. 
The curve of the AMM will be more fancy taking into the account the value of the time decay.  


### Functionality 

- Factory contract 
    - here manager can DP_ wtETH & YB_ wtETH AMM pool for every epoch
        - e.g. for epoch ending in June 2024 an AMM wtETH_0624 would be deployed

#### User actions

- Swapping tokens into the pool 
- LPing into the pool 


### Testnet reqeirements 

- only vanilla AMM is required
- for the price function $xy=k$ is sufficient




## Fixed yield module
This module allows for splitting 1 wtETH into two tokens, one pricipal token (1PT_ wtETH) and one interest token (1IT_ wtETH). One of which carries all the depeg risk of wtETH. 

### Functionality 

- Factory contract 
    - here manager calls function to deploy contracts for every epoch
        - a new fixed yield pool
        - PT_ wtETH & IT_ wtETH ERC20 contracts 
    - e.g. epoch ending in June 2024 would have tokens PT_ wtETH_0624 & IT_ wtETH_0624
- Redemption mechanism 
    - redeems PT_ wtETH & IT_ wtETH for underlying 
        - logic determining redemption before & after expiry 

#### User actions

- while pool active 
    - Depositing 
        - Deposit wtETH (receive 1 PT_wtETH & 1 IT_wtETH)
    - Withdrawing 
        - Deposit 1 PT_wtETH & 1 IT_wtETH (receive 1 wtETH)
- after pool deactivation
    - Redeeming 
        - Deposit PT_wtETH & IT_wtETH (receive wtETH, amount determined by the redemption function)


#### User journey

see example in litepaper [[t-protocol-docs/Tapir protocol litepaper v1.1#Example]]

### Components 

- **token splitting logic**
- **token redemption logic**
    - **redemption resolver** - logic determining at what amount of wtETH should PT_wtETH & IT_wtETH be redeemed at



### Lifecycle 

#### Fixed yield module 
Depeg module can be represented by a factory smart contract `FixedYieldFactory` that creates Fixed Yield pool instances, each instance defined by the time period of its creation. 

**Example**
To give a practical example, a  Fixed Yield pool could be created for 90 day duration and manager would create a pool 6 times per year, so that the whole year is covered with overlaps to allow for users having uninterrupted  Fixed Yield coverage.


####  Fixed Yield pools 


##### Initiation 
At this stage Depeg module manager initializes a pool by calling the function below on the `FixedYieldFactory` contract. He needs to define the pool duration `_poolActiveDuration` (e.g. active for 90 days).

the function description would look something like this: 
```solidity
function initFixedYieldPool(_poolActiveDuration) public onlyManager
```

This function will create 3 new contracts instaces, each name labelled with `241010`
- depeg pool instance `241010` contract (instances are labeled based on the day & month & year they have been created in in `YYMMDD` format, *Notice:* two pool instances should not be created in the single day to avoid confusion in naming of ERC20s)
- PT_wtETH ERC20 instance `241010` contract
- IT_ wtETH ERC20 instance `241010` contract 

At creation of a depeg pool these variables are set:
`initSharePrice = currentSharePrice()` defines the initial share price of wtETH at pool creation, this will be used to determine if depeg took place during the lifetime of the pool instance
`initializedAtBlock = current.block` defines at which block is the pool initialize
`deactivateAtBlock = current.block + _poolActiveDuration` defines at which block the pool becomes active 
`poolIsActive = True` this sets the pool to be active at the initialisation
`yieldResolved = false` this sets the fixed yield resolver to false at initialisation
##### Active pool interaction
Once the pool has been initiated, users can start interacting with the pool to split their `wtETH` into `PT_wtETH_241010` and `IT_wtETH_241010` or reverse the process.

```solidity

// for splitting 
function splitToken(_amount_of_wtETH) public {
    require(checkPoolIsActive())
    // 1. transfers wtETH from user
    // 2. mints PT_wtETH_241010 for the user in the amount 1*_amount_of_wtETH
    //    mints IT_wtETH_241010 for the user in the amount 1*_amount_of_wtETH
}

// for recombining split tokens 
function unSplitToken(_amount_of_wtETH_to_unsplit) public {
    require(checkPoolIsActive())
    // 1. transfers PT_wtETH_241010 and IT_wtETH_241010 from user in equal amounts _amount_of_wtETH_to_unsplit
    // 2. burns PT_wtETH_241010 for the user in the amount _amount_of_wtETH_to_unsplit
    //    burns IT_wtETH_241010 for the user in the amount _amount_of_wtETH_to_unsplit
    // 3. transfers wtETH to the user in _amount_of_wtETH_to_unsplit
}

// checks if pool is in active state
function checkPoolIsActive() public returns(bool) {
    if(current.block > deactivateAtBlock) {
    poolIsActive = false;
    }
    return poolIsActive; 
}


```

##### Yield resolution


Once the `deactivateAtBlock` block has been reached the pool is ready for redemptions. Redemption phase of the smart contract is can start once  `poolIsActive` is set to `false`.  The change of this variable is achieved by triggering any function, most directly by calling `checkPoolIsActive()`.


Once pool is no longer active, the yield needs to be resolved. This is done by calling `resolveYield()` which upon successful call will switch  `yieldResolved`  to `True`.  
This variable tells the pool at what price should the `PT` and `IT` assets be redeemed at. 

[!Note]
[@giorgi let's think of a best way to assure this]
> The function call `resolveYield()` is time sensitive and should be called right after the pool is deactivated. This is because it defines the value of  `PT` and `IT`, which is time sensitive and will change with passed time. 
> ?? can we try to update the pool state and resolve price depeg at every `sharePrice` update?  




```solidity

bool yieldResolved;


// checks current share price against the one at the beginning of the yield pool
function resolveYield() public {
    require(!checkPoolIsActive(), "the pool is still active")
    require(!yieldResolved, "the yield is already resolved")
    if(initSharePrice >= currentSharePrice()){
        interestTokenRatio = 0;
        principalTokenRatio = tokenDecimals;
    else {
    interestTokenRatio =  currentSharePrice()) / initSharePrice * tokenDecimals - tokenDecimals; // if interest is 1% for the duration of the pool, it should assign 1% * tokenDecimals
    principalTokenRatio = tokenDecimals - interestTokenRatio
    }

    yieldResolved = True;  
}


```


##### Funds redemption
Now users can redeem their `PT` and `IT` assets. They need to approve both ERC20s and call the function below.

```solidity

function redeemTokens(_amountPT, _amountIT) public {
    require(yieldResolved, "yield is not resolved");
    
    // 1. burns PT_wtETH_241010 and IT_wtETH_241010 from user's address in appropriate amounts specified in the input -> _amountPT, _amountIT
    // 2. calculates how much _amountWtETHtoSend to send for PT_wtETH_241010 and IT_wtETH_241010
    _amountWtETHtoSend = _amountPT*principalTokenRatio/tokenDecimals + _amountIT*interestTokenRatio/tokenDecimals
    // 3. send wtETH to the user 

}


```


