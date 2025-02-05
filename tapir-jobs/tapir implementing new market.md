# tapir implementing new market


## Goal 
- Implement this AMM code for our DP / YB pools. 
    - optimal
        - reusing this code "as is" -> it is audited & battle tested, one less thing to worry about. Adjust our code accordingly to be able to use code as is
    - less optimal 
        - adjust the given AMM in as minimal way as possible
- Create backend function that calculate all the inputs when creating a new AMM market

### Context 

#### theory 
- good description of the AMM Market, comparison with other similar ones 
    - [https://github.com/pendle-finance/pendle-v2-resources/blob/main/whitepapers/V2_AMM.pdf](https://github.com/pendle-finance/pendle-v2-resources/blob/main/whitepapers/V2_AMM.pdf)
        - this is the paper to take a look at btw, there is also comparison with other AMMs, the important thing is that the "Anchor rate" moves the price to keep the same implied yield rate in the AMM
          .e.g. If Implied yield of a AMM at the beginning of the year is 5%, it results in a completely different price than the same 5% implied yield at the end of the year. at the end of the year it results almost in 1 (1/~1.0001) while at the beginning of the year it is 1/1.05. 
          hope that makes intuitive sense.
          Scalar rate then defines the range, in which the AMM has a very low slippage, the tighter the range, the more capital efficient it is within this range, but then extremely capital inefficient outside that range. Meaning all of the liquidity is concentrated within this range. 
    - ![](https://i.imgur.com/H2ncTnC.png)




#### code 

[https://github.com/pendle-finance/pendle-core-v2-public/blob/main/contracts/core/Market/v3/PendleMarketFactoryV3.sol](https://github.com/pendle-finance/pendle-core-v2-public/blob/main/contracts/core/Market/v3/PendleMarketFactoryV3.sol)


here is the factory AMM market, that can launch other markets by this function

```
    /**
     * @notice Create a market between PT and its corresponding SY with scalar & anchor config.
     * Anyone is allowed to create a market on their own.
     */
    function createNewMarket(
        address PT,
        int256 scalarRoot,
        int256 initialAnchor,
        uint80 lnFeeRateRoot
    ) external returns (address market) {
```