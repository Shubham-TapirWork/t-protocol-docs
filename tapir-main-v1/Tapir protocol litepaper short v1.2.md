# Tapir protocol litepaper short v1.2

## Comment Suggest here!
https://hackmd.io/@WsWACVT3QOy5_gRc2Z3ZGg/rkE4o8lNyg

---


- [Overview](#Overview)
- [USP - unique selling proposition](#USP%20-%20unique%20selling%20proposition)
- [Go-to-Market Strategy](#Go-to-Market%20Strategy)
- [Token Incentives Strategy](#Token%20Incentives%20Strategy)
- [High-Level System Design](#High-Level%20System%20Design)
- [Modules](#Modules)
	- [Pool Module](#Pool%20Module)
	- [Depeg Protection Module](#Depeg%20Protection%20Module)
		- [What Makes This Depeg Protection Unique?](#What%20Makes%20This%20Depeg%20Protection%20Unique?)
		- [Unlocks](#Unlocks)
		- [Example](#Example)
			- [With depeg event](#With%20depeg%20event)
			- [With NO depeg event](#With%20NO%20depeg%20event)
		- [User incentives](#User%20incentives)
	- [Fixed yield module](#Fixed%20yield%20module)
		- [Why make this module?](#Why%20make%20this%20module?)
		- [Unlocks](#Unlocks)
		- [Example](#Example)
- [Takeaways](#Takeaways)
	- [Why Should Investors Care About tapir?](#Why%20Should%20Investors%20Care%20About%20tapir?)
	- [What Makes tapir Unique?](#What%20Makes%20tapir%20Unique?)


## Overview

Tapir protocol is a risk-adjusted, high-yield pooling platform offering tunable risk and reward profiles. Its depeg protection module helps risk-averse investors protect against slashings and other losses, enabling much higher yields than staking while offering much lower risk profile. At the same time, savvy investors can earn more by selling depeg protection. The protocol also supports a fixed yield option, appealing to those who value predictability, as well as leveraged yield strategies for investors comfortable taking on greater risk.

## USP - unique selling proposition

**Investors can buy protection against depegs**  
Tapir allows investors to buy or sell depeg protection against losses caused by events like hacks or slashings. This feature lets some investors earn extra by selling protection, while others sleep easier knowing they are covered. It addresses the challenge of balancing high yields with complex DeFi risks.

**Investors can further boost their yield**  
Beyond benefiting from standard yields, investors can sell depeg protection to earn additional premiums, effectively acting as underwriters. This creates new revenue streams and yield-enhancement opportunities not available in traditional investing methods.

**Investors can have a fixed yield**  
For those who prefer predictable returns, Tapir offers a fixed-yield option, mirroring traditional fixed-income investments. This choice delivers steady returns without unexpected yield fluctuations, ideal for conservative investors.

**Investors can have a leveraged long yield**  
Sophisticated investors can leverage their positions to amplify returns on the underlying yield. This allows them to capture multiple times the yield of conventional investing, making Tapir an attractive solution for informed investors seeking higher returns.

## Go-to-Market Strategy

Tapir will first target investors within the [Nektar Protocol](https://nektar.network/) ecosystem, leveraging existing relationships and the synergy of their high risk + yield decentralized marketplace. For the next integration we are considering Ethena & Pendle, due to their riskier nature & high yields. 

## Token Incentives Strategy

Tapir will reward early participants who provide initial liquidity and help reach Protocol Controlled Value (PCV) targets. By distributing native tokens to early investors, the protocol aligns incentives and encourages long-term commitment. Each round of incentives will have PCV milestones, ensuring measured growth. A lockup period may prevent rapid token churn, maintaining sustainable tokenomics. Over time, this controlled issuance supports stronger capital efficiency and appeal to other DeFi protocols.
For more on tokenomomics see **Tapir Tokenomics** document.

## High-Level System Design

The diagram below outlines the Tapir protocol’s architecture. Each module’s functionality is described in detail further on.

![[High level design combined.excalidraw | 1400]]  

![](https://i.imgur.com/5ItEgJa.png)

## Modules

Tapir comprises a core pooling module plus two additional modules, each offering unique functionalities.

### Pool Module

The Pool module gathers funds from investors and issues shares in return. These pooled assets are invested across various networks. It uses a native rebasing token, `tETH`, and a wrapped, non-rebasing version `wtETH` for use in other modules. This setup lays the foundation for flexible risk and yield management.

### Depeg Protection Module

This module allows users to buy or sell protection against protocol losses (depegs). A depeg occurs if `wtETH` at time $T_0$ is lower than at $T_{-1}$, indicating asset loss. By purchasing coverage with productive assets, investors maintain yield generation rather than holding idle capital.

#### What Makes This Depeg Protection Unique?

Unlike traditional insurance or derivative products that require holding non-productive assets, Tapir’s solution uses the underlying productive asset for protection. Capital isn’t idle—investors retain yield while being shielded from potential losses. This approach is more capital-efficient and profitable than other methods.

#### Unlocks

- **Derisking investment:** Buy depeg protection for safer yields.
- **Boosting yield:** Sell depeg protection to earn extra premiums while taking on more risk.

#### Example

**Assumption:** Maturity is 1 year.

Splitting 1 wtETH into 0.5DP + 0.5YB:

- **Derisking:** Alice trades her YB portion for DP. After trading at a hypothetical rate, she ends up with 0.99DP from her original 1 wtETH, gaining secure yield at the cost of some premium.
- **Boosting yield:** Bob buys YB tokens, positioning himself for higher returns but taking on potential double losses if a depeg occurs.

##### With depeg event

If a 5% depeg happens, Alice’s DP tokens protect her principal (0.99 wtETH), offering safe yield (~5.9% if assumed 7% yield). Bob, having sold protection, faces a loss (~2.7%).

##### With NO depeg event

Without a depeg, Bob enjoys boosted yields (~8%), while Alice earns  ~5.9%.

#### User incentives

- **DP_wtETH buyer:** Prioritizes safety and stable returns, willing to pay a premium.
- **YB_wtETH buyer:** Seeks higher fixed yields, confident that depegs are unlikely.

### Fixed yield module

#### Why make this module?

Some investors want fixed, predictable returns, while others seek leverage on variable yields. Integrating these features directly simplifies user experience and removes reliance on third parties. It also supports trading points and airdrops associated with the underlying tokens.

#### Unlocks

- **Fixing yield:** Holding only PT tokens reduces yield volatility.
- **Leveraged long yield:** Buying only YT tokens can magnify returns, it also allows users to buy only airdrop claims. 
- **Liquidity provisioning:** Providing liquidity in the fixed yield AMM to earn trading fees and manage exposure.

#### Example

Splitting 1 wtETH into 1PT + 1YT:

- **Fixing yield:** Alice buys PT to secure predictable returns.
- **Leveraged long yield:** Bob buys YT, hoping actual yields outperform predictions.
- **Liquidity provisioning:** Charlie provides liquidity by holding both PT and YT, earning fees while maintaining a balanced position.

## Takeaways

### Why Should Investors Care About tapir?

Tapir offers higher yields, customizable risk management, and flexibility not found in typical investing products. It provides insurance against slashing while still providing high yields. Investors who want stable returns can opt for fixed yields, while others seeking higher gains can leverage their positions. This adaptability makes the product appealing to a wide range of investors catering to varied preferences. 

### What Makes tapir Unique?

Its modular design and customizable strategies set it apart. Investors can mix and match components—depeg protection, fixed yield, leveraged yield—to tailor their investments. A risk-averse investor might pair fixed yield with depeg protection, while a more aggressive one might go all-in on leverage. This versatility empowers each investor to align strategy with personal risk appetite and return goals.