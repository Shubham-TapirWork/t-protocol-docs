# feedback web https://tapir.neveraportfol.io/ 2025-02-21

- issues 
    - does not prompt to change network to sepolia
- page
    - buy/sell view
        - missing "Regular token" view
            - think the agreement was to include this one as well
        - missing Yield-boosted asset description (see previous feedback)
        - Balance should probably not be DPtoken ![](https://i.imgur.com/LUi4ljz.png)
        - need description for "reward fee", also by this we mean "depeg protection cost" or something else? 
          IF yes, let's call it "depeg protection fee"
        ![](https://i.imgur.com/G8ETh2T.png)
            - NOTE we will also have Limit orders in the future
        - ? What do you think about having "market info section"
          ![](https://i.imgur.com/KxW6irD.png)
        - Include "expiry"
            - every pool has expiry and we need to show it to the user, see pendle 
              ![](https://i.imgur.com/O9n2jCS.png)
        - "Select a Strategy Above" - it is not clear from this what is ment by strategy, ?maybe have DP+Regular+YB all under "Strategy" umbrella? 
          ![](https://i.imgur.com/tCEwO1N.png)

            
    - ? position of  mode buttons? 
        - is it usual to put modes into right corner? my worry is that people will not notice (will the short tutorial solve it?)
            - have you considered moving it under asset directly? 
        - ![](https://i.imgur.com/fpZbxS4.png)
    - split view
        - Split ratio is fixed, we can remove the slider 
        - add "unsplit functionality" ?call it "unsplit" or "recombine"?
            - can be shaded out if user has no split tokens
    - liquidity view 
        - the A & B tokens either need to have fixed ratio (with current implementation)
          OR
          we need to handle swap on the frontend before adding liquidity 
          OR 
          we need to create special function 
            - pendle is using zaps for this
        - Include "expiry" in pool chart + above graph 
        - 