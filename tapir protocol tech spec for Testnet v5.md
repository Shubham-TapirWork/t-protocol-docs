# tapir protocol tech spec for Testnet v5

- [LRT module](#LRT%20module)
	- [Competition with the same functionality](#Competition%20with%20the%20same%20functionality)
	- [Functionality](#Functionality)
		- [User actions](#User%20actions)
	- [Components](#Components)
	- [Testnet requirements](#Testnet%20requirements)
- [Depeg protection module](#Depeg%20protection%20module)
	- [Functionality](#Functionality)
		- [User actions](#User%20actions)
		- [User journey](#User%20journey)
	- [Components](#Components)
	- [Lifecycle](#Lifecycle)
		- [Depeg module](#Depeg%20module)
		- [Depeg pools](#Depeg%20pools)
			- [Initiation](#Initiation)
			- [Depeg pool variables](#Depeg%20pool%20variables)
			- [Active pool interaction](#Active%20pool%20interaction)
				- [active functionality](#active%20functionality)
			- [Depeg resolution](#Depeg%20resolution)
				- [resolution functionality](#resolution%20functionality)
			- [Funds redemption](#Funds%20redemption)
				- [redemption functionality](#redemption%20functionality)
		- [Depeg AMM](#Depeg%20AMM)
			- [Initiation](#Initiation)
				- [Initial variables](#Initial%20variables)
			- [Active AMM interaction](#Active%20AMM%20interaction)
				- [AMM extra functionality](#AMM%20extra%20functionality)
			- [AMM Funds redemption](#AMM%20Funds%20redemption)
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



### Testnet requirements

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

This function will create 4 new contracts instances, each name labelled with `241010`
- depeg pool instance `241010` contract (instances are labeled based on the day & month & year they have been created in in `YYMMDD` format, *Notice:* two pool instances should not be created in the single day to avoid confusion in naming of ERC20s)
- DP ERC20 instance `241010` contract
- YB ERC20 instance `241010` contract 
- AMM for `YB` and `DP` ER20s. 

##### Depeg pool variables

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

For actually getting a yield boost or buying a depeg protection, users will need to swap their `DP` for `YB` or vice versa. For more on this see section [[tapir protocol tech spec for Testnet v5#Depeg AMM]] . 
Users can also earn rewards by LPing `YB` and `DP` assets into the AMM.
###### active functionality

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



###### resolution functionality

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
###### redemption functionality

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


#### Depeg AMM
Depeg AMM is an automatic market maker that allows market participants to buy or sell depeg protection. It holds asset `YB` and `DP` assets. As with any other AMM users could swap assets or provide liquidity. 
The AMM uses a stable swap curves with two adjustments. 
-  Asset price boundaries - There are trading boundaries at which swaps can be performed in only one way. 
- Time based price shift - The price shifts in time to account for the decrease in utility of the depeg swap 


##### Initiation 
This AMM is initialized at depeg pool initialization. Ideally by the `initDepegPool()` or by a separate function if needed. Initiation can also done after depeg pool has been initiated. 


###### Initial variables 
At initiation these variables need to be set: 

`address public DPTokenAddres` is an address of the `DP` token traded in this AMM
`address public YBTokenAddres` is an address of the `YB` token traded in this AMM
`initializedAtBlock = current.block` defines at which block is the AMM initialize
`deactivateAtBlock = current.block + _poolActiveDuration` defines at which block the pool becomes active 
`bool public tradingActive = True` This sets AMM to active state in which swaps are allowed
`bool public swappingPaused = False` Manager can pause swapping in case of a possible depeg event 


>[!Check if stableswap pools support this]
>`uint256 public initialDPprice` The initial price of DP. It is useful set this to achieve better capital efficiency, if the price is set implicitly just by the `DP / YB` ratio at innitial `addLiquidity()` not all funds can be utilized and efficiency is lost. 



> [!Implement Later]
> `uin256 DPPriceLowerBound` a lower bound at which the contract will not allow user to swap more `DP` for `YB`
> [!Note] This needs to be set to one, since there is no reason for `DP` to cost less than `YB`
> `uin256 DPPriceUpperBound` an upper bound at which the contract will not allow user to swap more `YB` for `DP`. 
> [!Note] This needs be set to an expected yield of `tETH`.  A price larger than this would imply a depeg event, after which trading needs to be stopped to prevent the draining of the AMM.
> 
> Timeshift needs to be incorporated into the swapping functionality to continually (block by block basis) shift the `DP` price downwards as the depeg pool is closer to maturity.  

##### Active AMM interaction 
Once AMM has been initiated users can `addLiquidity()`, `removeLiquidity()` and `swap()`. 
The functionality of the AMM is based on stable swap(think curve.fi pools) AMM. Here we explore only the added functionality on top of the original one. 



###### AMM extra functionality
```solidity

// **ADDITIONAL AMM FUNCTIONS** 

// checks if trading is active 
function checkTradingActive() public returns(bool) {
    if(current.block >= deactivateAtBlock) {
    tradingActive = false;
    }
    return tradingActive; 
}


// swaps cannot be performed after this fn is called successfully by the manager 
function freezeSwap() onlyManager {
    swappingPaused = True;
}


// can be called to revert freezeSwap() the above function
function unFreezeSwap() onlyManager {
    swappingPaused = False;
}



// **ADDITIONAL CHECKS IN SWAPPING** 

// before any swap there needs to be a check if pool is active and is not paused
function swap( ... ) ... {
    require(checkTradingActive(), "trading is not active")
    require(!swappingPaused, "trading is paused")
}


```

##### AMM Funds redemption
This is the phase after which trading ends and users can only remove liquidity from the AMM. This phase shift happens by either trying swap or directly calling `checkTradingActive()`.



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


