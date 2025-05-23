# tapir wireframes description



- [Landing Staking page - tapir.money](#Landing%20Staking%20page%20-%20tapir.money)
- [Stake page - app.tapir.money](#Stake%20page%20-%20app.tapir.money)

comment & edit here: 
https://hackmd.io/@WsWACVT3QOy5_gRc2Z3ZGg/r13McrW1ye

inspirations
https://www.ether.fi/
https://lido.fi/
https://claystack.com/


## Landing Staking page - tapir.money

Simple scrolling page, with the main banner focused on "Stake" "get high & safe yield"




**website Inspiration**
https://lido.fi/
https://claystack.com/



- elements 
    - - top ribbon 
        - Staking 
        - Docs (links to gitdocs) NO design needed
            - docs example https://docs.lido.fi/guides/node-operators/general-overview
        - About us 
            - TBD
        - ?Tokenomics
    - first window 
        - elements 
            - Left 
                - logo
            - Right 
                - show 4 different rows 
                    - Text + yield in different color (clickable links to stake page into appropriate ribbon)
                    - content of rows
                        - DP (Depeg protected safe yield) + [Yield]
                        - YB (Yield boosting aggressive yield) + [Yield]
                        - Reg (Regular restaking yield) + [Yield]
                        - LP (Yiled from liquidity provisioning) + [Yield]
                - Large "Stake" button under four rows -> links to app.tapir.money
        - https://lido.fi/ ![](https://i.imgur.com/kJbkpy8.png)
    - second window 
        - Why Tapir? 
            - 4 windows with icon plus text 
        - inspiration https://www.ether.fi/ ![](https://i.imgur.com/tPbtyAV.png)

    - third window 
        - Why Tapir? 
            - 4 windows with icon plus text 
        - inspiration https://www.ether.fi/ ![](https://i.imgur.com/tPbtyAV.png)

- others 
    - ecosystem partners
    - audits 
    - team 
    - investors 
    - 


## Stake page - app.tapir.money
- goal
    - clearly & simply show staking options
    - show ONLY necessary info 
- Elements 
    - Stake button 
    - Ribbon with 4 modes 
        - modes
            - DP(Depeg Protection)
            - YB(Yield Boost)
            - REG(Regular mode)
            - LP(Liquidity Provisioning)
            - Advanced(Manual mode)
            - Wrap
        - every mode has distinct 
            - show graph for this mode
            - show yield for this mode 
            - 1 sentence description about the mode with link to more info 
        - Manual mode extra 
- Default ribbon -> (DP- first ribbon)
 
**inspiration**
https://app.pendle.finance/trade/markets/0x6010676bc2534652ad1ef5fa8073dcf9ad7ebfbe/swap?view=yt&chain=ethereum

**stake view sketch**

![](https://i.imgur.com/ScYYO6Y.png)




### for MVP

#### functionality 

- investors need 
    - lido.fi has
        - buy tETH for ETH 
        - wrap tETH for wtETH 
    - we need to implement 3 staking modes
    - 
- MVP UI
    - for Desktop is sufficient 


#### wireframes 

##### 1st staking page 
this page should follow similar layout like https://lido.fi/. 

It should include logo on the left, 3 buttons with texts on the right (see texts below).  

###### functional difference
- three staking buttons instead of one that lido uses, after clicking, it takes user to **2nd staking page **


outline **with our texts**
![](https://i.imgur.com/X3g5G6e.png)

outline **with original texts**
![](https://i.imgur.com/VQk4NE8.png)
###### texts used 

![](https://i.imgur.com/fVeFcmM.png)

| 5%  |  |                     | Restake Safe                         |  |  |  |  |  |                                                                                                     |
|-----|--|---------------------|--------------------------------------|--|--|--|--|--|-----------------------------------------------------------------------------------------------------|
| apr |  | <discription under> | Restaking + buying depeg protection  |  |  |  |  |  | make all the colored ellements in the appropriate theme color (with regards to the type of staking) |
|     |  |                     |                                      |  |  |  |  |  |                                                                                                     |
| 7%  |  | <button>            | Restake with boost                   |  |  |  |  |  |                                                                                                     |
| apr |  | <discription under> | Restaking + selling depeg protection |  |  |  |  |  |                                                                                                     |
|     |  |                     |                                      |  |  |  |  |  |                                                                                                     |
| 6%  |  | <button>            | Restake only                         |  |  |  |  |  |                                                                                                     |
| apr |  | <discription under> | Regular restaking                    |


##### 2nd staking page 

this page should follow similar layout like https://stake.lido.fi/

It should include text on top (saying which staking it is), APR under and the staking button.
It should follow the color schema of the staking mode user clicks  

###### functional difference
- no added functionality on the page 
- we need 3 pages instead of one, one for each type of staking

![](https://i.imgur.com/6BRUs4U.png)


#### resources

main frontend to go off  
[lido.fi](http://lido.fi/)  
git  
[https://github.com/lidofinance/lido-frontend-template](https://github.com/lidofinance/lido-frontend-template)  
[https://github.com/lidofinance/ui](https://github.com/lidofinance/ui)perhaps some elements of uniswap interface could be usable, nothing must have from their repo  
[https://github.com/Uniswap/interface](https://github.com/Uniswap/interface) (edited)

logos, colors + other resources 
[https://docs.google.com/presentation/d/1OJzixBcMcLFENqKa9tXEn-PVvJ4aouJjnqIP0cQrJcw/edit?usp=sharing](https://docs.google.com/presentation/d/1OJzixBcMcLFENqKa9tXEn-PVvJ4aouJjnqIP0cQrJcw/edit?usp=sharing)


texts for the web in the table 