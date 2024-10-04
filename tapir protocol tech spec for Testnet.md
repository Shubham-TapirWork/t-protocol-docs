# tapir protocol tech spec for Testnet



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

see example in litepaper [[Tapir protocol litepaper v1#Example]]

### Components 

- **token splitting logic**
- **token redemption logic**
    - **depeg resolver** - logic resolving if there had been a depeg event and its size 
        - dependency
            - beacon oracle

### Testnet reqeirements 

- full functionality is required 


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