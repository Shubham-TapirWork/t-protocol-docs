# Tapir Tokenomics v2

## Comment / Suggest here!
https://hackmd.io/@WsWACVT3QOy5_gRc2Z3ZGg/Sk61yMkEke

---


- [Token Distribution](#Token%20Distribution)
		- [chart code](#chart%20code)
	- [Pie chart](#Pie%20chart)
- [DAO Operation](#DAO%20Operation)
- [Token Uses & Mechanisms](#Token%20Uses%20&%20Mechanisms)
	- [Governance](#Governance)
	- [Protocol Fees](#Protocol%20Fees)
	- [The Burn Mechanism](#The%20Burn%20Mechanism)
- [Vesting Periods](#Vesting%20Periods)
	- [Investors, Advisors & Team](#Investors,%20Advisors%20&%20Team)
	- [Incentivization Programs](#Incentivization%20Programs)
	- [Sustainability and Value Capture for Stakeholders](#Sustainability%20and%20Value%20Capture%20for%20Stakeholders)
- [Token Incentives](#Token%20Incentives)
	- [Goals](#Goals)
	- [Lockup](#Lockup)
	- [Control Mechanism](#Control%20Mechanism)
		- [Detailed Control Mechanisms](#Detailed%20Control%20Mechanisms)
- [Summary](#Summary)
- [Conclusion](#Conclusion)





## Token Distribution

#### chart code 
```python
import matplotlib.pyplot as plt

# Data for the updated token distribution
labels = ['Token Public Sale (30%)', 'Token Presale (10%)', 'Protocol Partnerships (10%)', 'Core Team & Advisors (20%)', 'Incentives (20%)', 'Reserve (10%)']
sizes = [30, 10, 10, 20, 20, 10]
colors = ['#ff9999', '#66b3ff', '#99ff99', '#ffcc99', '#c2c2f0', '#ffb3e6']

# Plotting the pie chart
plt.figure(figsize=(8, 8))
plt.pie(sizes, labels=labels, colors=colors, autopct='%1.1f%%', startangle=140, wedgeprops={'edgecolor': 'black'})
plt.title('Updated Token Distribution')
plt.axis('equal')  # Equal aspect ratio ensures that pie is drawn as a circle.

# Show the chart
plt.show()
```

### Pie chart

![](https://i.imgur.com/n401fjc.png)



The token distribution is divided as follows:

**40% Token Public Sale**: These tokens will be sold gradually to the public through various platforms, with tokens being unlocked immediately upon sale.

**10% Token Presale**: These tokens will be sold to early investors and are a subject to lockup.

**10% Protocol Partnerships**: These tokens are locked and vested over a set period to ensure commitment from partners.

**20% Core Team & Advisors**: Allocated to the core team and advisors, these tokens are locked and vested, providing motivation and aligning interests with the protocol's success.

**20% Incentives**: These tokens are set aside for incentives, locked and vested to reward early adopters and contributors.

**10% Reserve**: Held in the treasury for future strategic initiatives or unforeseen needs.

## DAO Operation
All funds raised from the token sale are deposited into the treasury. The core team submits proposals to the DAO to receive payments from the treasury, ensuring that all spending is transparent and approved by governance.


## Token Uses & Mechanisms
### Governance
The primary use of the token is to participate in governance. Token holders can direct the DAO, make decisions regarding the budget, and prioritize protocol initiatives.

### Protocol Fees
The protocol charges two types of fees:

- **Withdrawal Fee**: A fee of 0.5% is applied when users withdraw ETH from the system using the `withdraw()` function.
- **Success Fee**: A 1% success fee is charged on the `rebase()` function, contributing 1% of the generated rewards to the DAO.

### The Burn Mechanism
Half of the collected protocol fees are burned to remove tokens from circulation, effectively reducing supply and increasing scarcity. The remaining 50% is sent to the DAO treasury for future use. The burn process is managed by a dedicated burn smart contract. Periodically, the DAO will trigger the burn function to swap accumulated fees for TPR tokens, which are then burned to lower the total supply.

## Vesting Periods
### Investors, Advisors & Team
A **one-year cliff** is applied for investors, advisors, and team members, starting from the mainnet contract deployment date. After this cliff, tokens are unlocked linearly over the following year.

For example, if an advisor receives token allocations, they will only have access to these tokens after the one-year cliff, with gradual access over the next year.

### Incentivization Programs
Tokens claimed as rewards from incentivization programs are subject to a **one-year lock**. For instance, if a user claims tokens from an incentivization program, these tokens will be locked for one year from the date of the claim, ensuring long-term commitment to the protocol.

> Gas requirements for these claims should also be considered.

### Sustainability and Value Capture for Stakeholders
For investors, value is driven by the burn mechanism, reducing token supply and increasing scarcity. Stakers and operators will receive TPR rewards during the early stages of the protocol to help bootstrap the project. The goal is to align these stakeholders with the protocol's long-term vision, encouraging them to retain their tokens and participate as long-term stakeholders.

## Token Incentives
### Goals
We do not believe that pointless "gamified" quests bring anything of tangible value to the project long term.  

The primary goal of token incentives is to improve the product experience. A secondary goal is to accelerate protocol growth. Specifically, increasing total value locked (TVL) and liquidity for depeg protection trading is essential not just for vanity metrics but for reducing slippage and enhancing the user experience.

The tokenomics structure has well-defined goals along with control mechanisms to ensure efficient allocation without overpaying. The objectives are:

- Attract TVL to the project.
- Ensure sufficient liquidity for depeg protection trading.

In each epoch, specific targets are set for TVL and liquidity, aligning governance token distribution with protocol growth. A lockup period will also be applied to prevent automated token farming and ensure long-term commitment from recipients. 


Reaching TVL targets quickly is important for capital efficiency and will help the protocol be accepted as collateral in other DeFi platforms.

### Lockup 
All TPR received via incentives will be subject to the same one year lockup period. That is, the claimed tokens will be transferable after one year. 

### Control Mechanism
To bring TVL to the project, the mechanism targets specific TVL within a defined timeframe and distributes TPR tokens on a pro-rata basis. Similarly, to ensure sufficient liquidity for depeg protection trading, predefined pool liquidity is targeted, with TPR tokens distributed accordingly.

A feedback loop is used to target specific metrics, such as TVL and pool liquidity, and distribute tokens accordingly:

- A fixed number of tokens (e.g., 10,000 TPR per week) may be distributed until a target TVL (e.g., 1,000 ETH) is reached.
- **If TVL Exceeds the Target**: If TVL exceeds the target by 20%, rewards in next round will decrease to prevent excessive dilution.
- **If TVL Falls Below the Target**: If TVL falls below the target buffer, rewards will be maintained to encourage new capital inflows.
    - A maximum cap (e.g., 1,000 TPR per ETH) will also be used to prevent excessive dilution.

#### Detailed Control Mechanisms
The control mechanisms are designed to ensure efficient resource allocation while maintaining a balance between incentivizing growth and avoiding dilution. Below are some expanded details on how the control mechanisms operate:

1. **Epoch-Based Distribution**: Tokens are distributed based on epochs, which are predefined time intervals during which specific goals must be reached. For example, during each epoch, a fixed amount of TPR tokens is allocated for distribution based on the TVL and liquidity targets set for that epoch. This ensures there is a predictable, periodic injection of incentives, making it easier to evaluate the protocol's growth.

2. **Dynamic Adjustment of Rewards**: The rewards are dynamically adjusted based on the performance of the protocol:
   - If the **TVL rises significantly** above the target (e.g., by 20%), the rewards allocated for the subsequent epochs are gradually reduced. This prevents over-incentivization and helps protect the value of the TPR token from excessive dilution.
   - Conversely, if the **TVL drops below the target threshold**, the rewards are kept steady or even increased to incentivize new deposits and capital inflow. This flexible approach ensures that incentives are aligned with the protocol’s needs at different stages of growth.

3. **Pro-Rata Basis for Fair Distribution**: Token distribution is carried out on a pro-rata basis, meaning that rewards are distributed proportionally to the contribution of participants. For example, liquidity providers who contribute more to the protocol’s TVL will receive a larger share of the allocated tokens compared to smaller contributors. This helps ensure fairness and aligns incentives with the scale of the contribution.

4. **Cap on Maximum TPR per ETH**: To prevent excessive dilution, a cap is imposed on the maximum TPR tokens that can be earned per ETH (e.g., 1,000 TPR per ETH). This cap is crucial for maintaining the balance between incentivizing participants and protecting the value of the token. It prevents disproportionate rewards that could result in large-scale dilution and potential instability in the token’s value.

5. **Feedback Loop for Continual Adjustment**: The protocol implements a feedback loop where the target metrics, TVL and pool liquidity are adjusted after every epoch. This is to ensure that the protocol's objectives are met without overpaying. For instance, if the liquidity pool consistently exceeds the target, rewards can be reallocated towards other areas that need growth, ensuring the efficient use of resources.

6. **Targeting Multiple Metrics**: While TVL is an important metric, the control mechanisms also targets **liquidity for depeg protection trading**. By setting specific liquidity targets, the protocol ensures that there is always sufficient liquidity available for users. This enhances the overall user experience by reducing slippage and ensuring smooth trading operations, which is particularly important during periods of high market volatility.

7. **Preventing Automated Farming**: To mitigate the risk of automated token farming, the protocol includes a **lockup period** for distributed tokens. This means that even after tokens are earned as rewards, they cannot be immediately sold or transferred. This lockup encourages long-term commitment to the protocol and aligns the incentives of all participants with the protocol's sustainable growth.

8. **Example Scenario**: Imagine the protocol is aiming for a TVL target of 1,000 ETH. During the first epoch, 10,000 TPR tokens are distributed weekly to liquidity providers. If the TVL reaches 1,200 ETH (20% above the target), the rewards for the next epoch might be reduced to 7,500 TPR per week to avoid over-incentivizing. If the TVL drops to 800 ETH (20% below the target), the rewards might be adjusted back to 10,000 TPR or even increased to 12,000 TPR to attract more capital and bring TVL back to the desired level.

These mechanisms collectively help maintain a balanced and sustainable growth trajectory for the protocol, ensuring that incentives are effectively aligned with long-term success without compromising the value of the TPR token.

## Summary

Tapir Tokenomics aims to foster sustainable growth, align incentives, and ensure the long-term success of the Tapir protocol. The token distribution balances public sale, incentivization, partnerships, team rewards, and future strategic initiatives. Governance is central to token use, allowing stakeholders to influence decision-making.

Protocol fees are collected through a withdrawal fee and a success fee, with a portion burned to manage token supply. Token incentives attract liquidity, grow Total Value Locked (TVL), and ensure sufficient liquidity for depeg protection trading.

Vesting periods and lockups ensure long-term commitment from investors, team members, and participants in incentivization programs. The goal is to create a thriving ecosystem where stakeholders capture value through active involvement.

## Conclusion

Tapir Tokenomics blends token distribution, governance, and incentivization to support sustainable growth. By implementing vesting periods, control mechanisms, and balanced token allocation, Tapir aims to align participants, reduce slippage, and achieve capital efficiency.

The governance model empowers stakeholders, while the burn mechanism contributes to value capture and scarcity. Ultimately, Tapir Tokenomics focuses on creating a secure, efficient, and user-friendly experience that drives growth and long-term value for all participants.