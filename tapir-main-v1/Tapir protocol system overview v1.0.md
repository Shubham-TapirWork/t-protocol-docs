# Tapir protocol system overview v1.0


## Comment Suggest here! 
https://hackmd.io/@WsWACVT3QOy5_gRc2Z3ZGg/rJzk5niyJl

## Table of content

[TOC]

## Overview

Tapir protocol is an native LRT with **LRT with tunable risk & yield.**

The depeg protection module allows for protecting risk averse investors against slashing risk unlocking much higher yield than regular ETH staking rewards without the risks of restaking. It also enables sophisticated investors who can estimate restaking risks to boost their yield by selling this protection.

Fixed yield is a preferred vehicle for many investors, as seen in traditional markets It also allows for a leveraged long yield strategy which sophisticated investors can leverage to earn multiples of restaking yield.


## USP - unique selling proposition

**Investors can buy protection against slashing**

Restakers will have the ability to either sell or purchase depeg protection (protection against slashing), which will either boost their yield or allow them to sleep easier by protecting themselves against depeg events.

This solves the main pain-point that restaking investors are now facing. Every staker would rather have higher restaking yields, but not many become restakers since it is hard to reason about the heterogeneous risk that restaking brings. With tapir they will be able to enjoy restaking yields with safety characteristics of staking. 


**Investors can further boost their yield**

Restakers not only have the opportunity to benefit from restaking yields, but they can also significantly enhance their returns by selling depeg protection to other investors. This feature is particularly attractive to those who are confident in the evaluating the AVS slashing risks. 

By offering protection to others, these investors effectively act as underwriters, and in return, they collect premiums that directly increase their overall yield. This strategy opens up an additional revenue stream, allowing restakers to leverage their position and maximize profits in ways that were previously unavailable in traditional staking models.

**Investors can have a fixed yield**

For investors who prioritize stability and predictability, Tapir offers the ability to secure a fixed yield for their restaking investments. This product mimics the appeal of traditional financial instruments where fixed-income investments are preferred by those looking for steady returns with lower risk. By opting for this fixed yield, investors can enjoy restaking benefits without being exposed to volatile or unpredictable yield fluctuations. It’s a tailored solution for conservative investors seeking dependable, consistent returns while still participating in the restaking ecosystem.

**Investors can have a leveraged long yield**

For more sophisticated or risk-tolerant investors, Tapir unlocks the possibility to multiply their earnings by taking a leveraged long position on restaking yields. This option allows them to amplify their exposure to the upside potential of restaking yields, capturing multiples of what they could earn with traditional restaking. By strategically increasing their leverage, these investors stand to benefit significantly from market movements, turning restaking into a high-return opportunity. This is ideal for investors who understand the dynamics of the restaking space and want to maximize their return on investment while managing their risk exposure according to their personal strategy.


## Go-to-Market Strategy

The initial target audience will be restakers within the [Nektar Restaking Protocol](https://nektar.network/) ecosystem, leveraging the close connection between the founders of both projects. The strategy is to first introduce the LRT (Liquid Restaking Token) on this platform, positioning it as one of the pioneering LRTs and establishing a dominant presence within Nektar's ecosystem. Once a strong foothold is secured, the expansion will continue to other restaking platforms.

Nektar’s use of DVT (Distributed Validator Technology) further reduces risk for restakers, creating a natural synergy between our risk-aware LRT protocol and their risk-minimized restaking platform. This alignment strengthens the value proposition for both projects, making Nektar the ideal launchpad for our initial rollout.

After gaining traction in the Nektar ecosystem, the focus will shift to capturing other smaller restaking platforms like Karak and Symbiotic. The long-term goal is to then allocate business development resources towards entering larger ecosystems, such as Eigenlayer.

## Token Incentives Strategy

The token incentives strategy focuses on driving aggressive growth by rewarding early adopters with the protocol’s native token. These rewards will be distributed to early stakers who provide the necessary capital to bootstrap the project. Each incentivization round will have specific Protocol Controlled Value (PCV) targets, ensuring that growth is carefully measured and aligned with the protocol’s long-term goals. This approach will help redistribute tokens to early stakeholders, creating a vested interest in the project’s success. Additionally, a lockup period may be implemented to prevent automated token farming and promote long-term alignment with the protocol’s vision.

By setting concrete PCV targets, the protocol can regulate token issuance efficiently, ensuring that growth is not overpaid for and that incentives remain sustainable. As the protocol scales, it will benefit from greater capital efficiency, increasing its attractiveness as collateral for other DeFi protocols.

Key objectives include:

- Rapidly achieving PCV targets
- Turning early adopters into stakeholders and protocol evangelists

The strategy will monitor these outcomes and create a feedback loop to control token inflation, preventing excessive rewards and ensuring sustainable, well-aligned growth.

## Modules

The protocol is built around a core pooling module for gathering and allocating funds, along with two additional modules that provide its unique features.

### LRT Module

The LRT (Liquid Restaking Token) module is responsible for pooling funds from restakers and minting LRTs in exchange. These pooled funds are then allocated to various strategies, primarily deployment across different restaking networks. This module functions similarly to competitive offerings in the market, but it forms the foundation of the protocol’s functionality.

The module operates with a native rebasing token, `tETH`, which continuously adjusts to reflect the underlying yield. For users who prefer a non-rebasing token, `tETH` can be wrapped into `wtETH`, offering a stable representation of the underlying asset. 

The non-rebasing `wtETH` will be utilized in the Depeg Protection and Fixed Yield modules, enabling investors to tailor their risk and reward preferences while participating in the protocol.

### Fixed yield module

#### Why to make this module?

The more conservative investors prefer to remove variability from their yield and fix it. On the other hand the more sophisticated ones may prefer to leverage their yield, by selling the fixed part and buy the variable one. It can also be used as a tool for selling & purchasing points and an airdrop associated with them. As we have seen, this proved very popular feature in the past few months

There are other protocols with this feature, however it is quite advantageous to integrate it directly into the core protocol as this removes any external dependencies on the third parties & allows us to tailor it specifically to our use case.


#### Unlocks

This module unlocks these yield strategies & their combination:

- **fixing yield** by keeping only PT token thus decreasing yield volatility
- **leveraged long yield**, by buying only YT tokens. A high risk strategy that could carry large yields
- **liquidity provisioning** in the fixed yield AMM. This could be done in a yield neutral way(keeping proportional LP+YT exposure) or more geared towards fixed yield (keeping LP only).

#### Example

split - 1 wtETH => 1PT +1YT

- fixing yield
    - Alice wants to fix her yield thus she will purchase 1PT_wtETH for her wtETH. Alternatively she could split her wtETH and sell the YT token for PT at later date if she thinks the price will be more favorable.
- leveraged long yield
    - Bob believes that wtETH's yield will be higher than YT_wtETH's price implies. If he is right he can have a high leverage on this trade by just purchasing YT_wtETH for his wtETH.
- liquidity provisioning
    - Charlie believes that many users will want to trade this fixed yield, thus he wants to earn the trading fees and provide liquidity.
    - Thus he will sell portion of his wtETH for PT_wtETH which he needs in order to become LP. His effective position is having some part of his yield fixed while some part not. Both of these tokens carry yield, but under certain conditions it might be more beneficial to own just one of them.



### Depeg Protection Module

This module enables users to buy or sell protection against depeg events. A depeg is defined as any situation where the value of `wtETH` at time ${T_0}$ is lower than its value at time $T_{-1}$ $wtETH_{T_0} < wtETH_{T_{-1}}$ . In simpler terms, a depeg occurs when there is a loss of funds within the protocol, often caused by slashing.

#### What Makes This Depeg Protection Unique?

While there are various ways for investors to safeguard against depeg events—such as purchasing insurance products, options, or derivatives—this module stands out because it allows users to retain 100% of the yield from the underlying asset while being protected. Traditional insurance products and options are typically denominated in non-productive assets like USD or ETH, which means those assets do not generate yield. 

This module is unique in its capital efficiency, as the protection is bought using the underlying asset itself, not in non-productive assets like ETH or USD. As a result, there is no "dead" capital sitting idle, unlike in other protection mechanisms. The capital remains productive while still offering the same level of protection, making it a more efficient solution for restakers who want to balance risk and yield without sacrificing growth potential.

#### Unlocks

This module unlocks these yield strategies & their combination:

- **derisking investment** by purchasing depeg protection
- **boosting yield** by selling depeg protection and taking on additional risk

#### User incentives

**YT_wtETH buyer** this user believes the future wtETH yield will be higher than the expected yield implied by YT_wtETH price. Also, there is an implied premium with taking on variable yield and selling the fixed part.

**wtETH buyer** this user believes the future wtETH yield will be lower than the expected yield implied by YT_wtETH price. Alternatively he may be willing to pay premium for fixing his yield.

**DP_ wtETH buyer** this user wants as safe yield profile as possible. This product allows him to both fix the future restaking yield as well as protect against depeg event. He is willing to pay for this in terms of decreased yield.

**YB_ wtETH buyer** this user is looking for the highest fixed yield possible. He does not believe that wtETH depeg is likely and is willing sell the DP_ wtETH in order to boost yields.

## Takeaways

### Why Should Investors Care About Another LRT?

This LRT introduces a compelling combination of higher yield potential and customizable risk management, attracting a broad spectrum of investors. The depeg protection feature enables investors to shield themselves from slashing risks, offering the advantage of restaking yields with the same security as traditional staking. For those who are comfortable with assuming risk, selling depeg protection becomes an additional source of income, effectively increasing their overall yield by acting as underwriters to the ecosystem.

Moreover, the LRT provides tailored investment strategies that go beyond simple staking. Conservative investors can opt for a fixed yield, ensuring stability and predictability in their returns, similar to traditional fixed-income assets. At the same time, more aggressive investors can choose leveraged positions to significantly amplify their earnings. This versatility allows investors to align their investments with their individual risk tolerance and return goals, making the LRT an adaptable tool for varying financial strategies.

### What Makes This LRT Unique?

What truly distinguishes this LRT is its modular structure, allowing investors to fine-tune their risk and yield preferences in ways that traditional staking products cannot offer. 

**Express Risk & Yield Preferences:** Investors can choose between higher yields with increased risk or lower-risk, more stable returns. They also have the option to lock in a fixed yield, offering a more controlled return profile. This flexibility caters to sophisticated investors who have been cautious about entering the LRT market due to its perceived complexity.

The ability to mix and match these modules adds another layer of customization. For example, a risk-averse investor might combine a fixed yield strategy with depeg protection, creating a more secure investment while still participating in restaking’s yield potential. This modular approach offers unparalleled flexibility, allowing each investor to craft a strategy that matches their individual risk appetite and financial objectives.
