# tapir frontend app wireframes description


comment & edit here



## Stake page - app.tapir.money
- goal
    - clearly & simply show staking options
    - show ONLY necessary info 
- Elements 
    - Stake button 
    - Ribbon with 4 modes 
        - modes (see the sketch below)
            - DP(Depeg Protection)
            - YB(Yield Boost)
            - REG(Regular mode)
            - LP(Liquidity Provisioning)
            - Advanced(on pic below - Manual mode)
            - Wrap
        - every mode has distinct 
            - show graph for this mode
            - show yield for this mode 
            - 1 sentence description about the mode with link to more info 
        - Manual mode extra 
- Default ribbon -> (DP- first ribbon)
 
**inspiration**
https://app.pendle.finance/trade/markets/0x6010676bc2534652ad1ef5fa8073dcf9ad7ebfbe/swap?view=yt&chain=ethereum

https://app.uniswap.org/positions/create/v3?currencyA=0x2260FAC5E5542a773Aa44fBCfeDf7C193bc2C599&currencyB=NATIVE&chain=ethereum


**stake view sketch**

![](https://i.imgur.com/ScYYO6Y.png)




### User actions 

#### Regular staker 
think of user of lido or staking protocol, no deeper understanding of protocol expected


These are the most frequent actions users are expected to take: 
- Staking 
    - different types of staking users can do (buttons)
        - `safe stake`
        - `boosted stake`
        - `stake`

#### Liquidity provider 
knowledge from other AMMs on how LP works expected


User's providing liquidity need to be able to managed their positions: 
- Market (AMM pool) interactions 
    - different actions regarding market interaciton
        - `swap`
        - `add liquidity`
        - `remove liquidity`


#### Advanced protocol user 
a defi degen, understands multiple defi protocols, he is not expected to need to read the docs first, to understand what he is about to do should be clear from the view.

This action is for advanced user who want to manually control splitting / unsplitting of their token. 

- Token splitting
    - actions regarding splitting & unsplitting the `wtETH` token
        - `split`
        - `unsplit`

### Notes for Wireframe 

- you can take the pic above as an inspiration and do its variation or propose something completely new

- wireframes should include 
    - clear layout of the page & subpages to perform all the user actions
    - make the view simple for regular user but also allow advanced user to have a clear understanding of the interactions he will be taking 



- 