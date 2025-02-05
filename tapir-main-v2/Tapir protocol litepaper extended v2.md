# Tapir protocol litepaper extended v2



- [Comment Suggest here!](#Comment%20Suggest%20here!)
- [Overview](#Overview)
- [USP - unique selling proposition](#USP%20-%20unique%20selling%20proposition)
- [Go-to-Market Strategy](#Go-to-Market%20Strategy)
- [Token Incentives Strategy](#Token%20Incentives%20Strategy)
- [High-Level System Design](#High-Level%20System%20Design)
- [Modules](#Modules)
	- [Depeg Protection Module](#Depeg%20Protection%20Module)
		- [What Makes This Depeg Protection Unique?](#What%20Makes%20This%20Depeg%20Protection%20Unique?)
		- [Schematic outline](#Schematic%20outline)
		- [Unlocks](#Unlocks)
		- [Example](#Example)
			- [With depeg event](#With%20depeg%20event)
			- [With NO depeg event](#With%20NO%20depeg%20event)
		- [User incentives](#User%20incentives)
- [Takeaways](#Takeaways)
	- [Why Should Investors Care About tapir?](#Why%20Should%20Investors%20Care%20About%20tapir?)
	- [What Makes tapir Unique?](#What%20Makes%20tapir%20Unique?)

## Comment Suggest here! 


## Overview

Tapir protocol is a depeg protection marketplace. 
It allows users to derisk their defi investment or earn additional yield by either buying or selling the depeg protection. Our unique competitive advantage is that both the depeg protection buyers and sellers keep the full yield of the underlying protocol. This is something no other similar solution can offer and makes Tapir best suited for integrating with high yield protocols. 

## USP - unique selling proposition

No one has been able to offer protection for the high yield assets. 
The reason is simple, the protection sellers are undergoing the same risk as if they were holding the risk asset, but leaving all the juicy yield on the table. Tapir is unique in preserving the base yield for both the buyers & sellers.

**Investors can buy protection against depegs**  
Tapir allows investors to buy or sell depeg protection against losses caused by events like hacks or slashings. This feature lets some investors earn extra by selling protection, while others sleep easier knowing they are covered. It addresses the challenge of balancing high yields with complex DeFi risks.

**Investors can further boost their yield**  
Beyond benefiting from standard yields, investors can sell depeg protection to earn additional premiums, effectively acting as underwriters. This creates new revenue streams and yield-enhancement opportunities not available in traditional investing methods.

## Go-to-Market Strategy

Tapir will first target investors within the pendle ecosystem. This seems like the best protocol to integrate with, due the high fix yield yield that is being offered on the its assets, where the highest yield ones are usually the newest & most risky ones. Also Pendle offers many assets from many different underlying protocols, so by integrating with them we effectively allow user to participate in all the different protocols that Pendle integrates, without the need of integrating them directly. 

## Token Incentives Strategy

The token incentives strategy focuses on driving aggressive growth by rewarding early adopters with the protocol’s native token. These rewards will be distributed to early stakers who provide the necessary capital to bootstrap the project. Each incentivization round will have specific Protocol Controlled Value (PCV) targets, ensuring that growth is carefully measured and aligned with the protocol’s long-term goals. This approach will help redistribute tokens to early stakeholders, creating a vested interest in the project’s success. Additionally, a lockup period may be implemented to prevent automated token farming and promote long-term alignment with the protocol’s vision.

By setting concrete PCV targets, the protocol can regulate token issuance efficiently, ensuring that growth is not overpaid for and that incentives remain sustainable. As the protocol scales, it will benefit from greater capital efficiency, increasing its attractiveness as collateral for other DeFi protocols.

Key objectives include:

- Rapidly achieving PCV targets
- Turning early adopters into stakeholders and protocol evangelists

The strategy will monitor these outcomes and create a feedback loop to control token inflation, preventing excessive rewards and ensuring sustainable, well-aligned growth.

## High-Level System Design

The following schema provides an overview of the system's architecture. Each module is detailed below, outlining its functionality and role within the overall design.


![[High level design combined v2.excalidraw | 1400]]


![](https://i.imgur.com/6wuNVY1.png)





## Modules

The protocol is built around a core pooling module for gathering and allocating funds, along with two additional modules that provide its unique features.


### Depeg Protection Module

This module enables users to buy or sell protection against depeg events. A depeg is defined as any situation where the value of `token_A` at time ${T_0}$ is lower than its value at time $T_{-1}$ $token_A_{T_0} < token_A_{T_{-1}}$ . In simpler terms, a depeg occurs when there is a loss of funds within the protocol, often caused by slashing.

#### What Makes This Depeg Protection Unique?

While there are various ways for investors to safeguard against depeg events—such as purchasing insurance products, options, or derivatives—this module stands out because it allows users to retain 100% of the yield from the underlying asset while being protected. Traditional insurance products and options are typically denominated in non-productive assets like USD or ETH, which means those assets do not generate yield. 

This module is unique in its capital efficiency, as the protection is bought using the underlying asset itself, not in non-productive assets like ETH or USD. As a result, there is no "dead" capital sitting idle, unlike in other protection mechanisms. The capital remains productive while still offering the same level of protection, making it a more efficient solution for Investors who want to balance risk and yield without sacrificing growth potential.

#### Schematic outline

![](https://i.imgur.com/MiUU154.png)


![[Depeg Protection module v2 2024-08-26 11.22.21.excalidraw| 1000]]

#### Unlocks

This module unlocks these yield strategies & their combination:

- **derisking investment** by purchasing depeg protection
- **boosting yield** by selling depeg protection and taking on additional risk

#### Example

**Assumption** We assume that the maturity period is **1 year** in this calculation, for sake of greater clarity, however, the actual maturity could be different.

split - 1 token_A => 0.5DP + 0.5YB

- In this step Alice splits token_A into 0.5DP_ token_A and 0.5YB_ token_A
    - derisking investment
        - If she wants depeg protection she will sell the yield boosted part (0.5YB_ token_A) for depeg protected part (DP_ token_A).
        - Let's assume the price for YB_ token_A is 1.02 YB_ token_A/DP_ token_A. Thus by selling 0.5YB_ token_A, she will be able to get 0.49DP_ token_A(0.5/1.02). Thus Alice's initial position of 1 token_A will translate into 0.99DP_ token_A(0.5minted+0.49bought).
    - boosting yield
        - Conversely Bob based on his calculations believes that the risk adjusted return of selling the depeg protection is warranted and he is willing to take the other side of the trade that Alice is making. Thus Bob's initial position of 1 token_A will translate into 1.01YB_ token_A(0.5minted+0.51bought).

##### With depeg event

Let's assume 5% depeg of the token_A at expiry, let's continue with Alice's & Bob's position from the previous example.

Alice holds 0.99DP_ token_A. Holding a DP token entitles her to redeem her depeg protection token one to one at expiry. Hence she can redeem 0.99DP_ token_A for 0.99 token_A. The pool holding the token_A will redeem 100% of DP_ token_A and 90% YB_ token_A(1-2x(0.05)).

Alice will receive her full amount of PT tokens she is entitled to by her position of 0.99DP_ token_A. If we were to assume that the implied yield of token_A is 7% her effective profit is ~5.9%(1.07x0.99x1). It is important to note that she can lock in this profit at the time of purchasing the depeg protection. The only caveat is that the depeg event must be less or equal to 50%. (This is implied by the structure of the token split). Thus her cost of insurance is ~1%.

On the other hand Bob receives 101% of the fixed profit of PT token but he is also exposed to double the depeg risk since his YB token covers the depeg loss for Alice's DP token. If we assume that the implied yield of token_A is 7% his effective loss is ~2.7%(1.07x1.01x0.9-1).

##### With NO depeg event

Bob's position under no depeg event translates into ~8%(1.07x1.01x1) yield, meaning his yield is boosted by 1%, while Alice's position(0.99DP_ token_A) translates into the same ~5.9%(1.07x0.99x1).

**NOTE** Note that there is no "dead"(undeployed) capital in the system. Both Alice and Bob are fully exposed to the underlying.

#### User incentives

**YT_token_A buyer** this user believes the future token_A yield will be higher than the expected yield implied by YT_token_A price. Also, there is an implied premium with taking on variable yield and selling the fixed part.

**token_A buyer** this user believes the future token_A yield will be lower than the expected yield implied by YT_token_A price. Alternatively he may be willing to pay premium for fixing his yield.

**DP_ token_A buyer** this user wants as safe yield profile as possible. This product allows him to both fix the future investing yield as well as protect against depeg event. He is willing to pay for this in terms of decreased yield.

**YB_ token_A buyer** this user is looking for the highest fixed yield possible. He does not believe that token_A depeg is likely and is willing sell the DP_ token_A in order to boost yields.


## Takeaways

### Why Should Investors Care About tapir?

Tapir offers higher yields and customizable risk management. It provides insurance against smart contract hacks, slashings and other depeg events while still keeping the high base yields. This adaptability makes the product appealing to a wide range of investors catering to their varied preferences. 

### What Makes tapir Unique?

The ability keep all the base yield for both parties. This unprecedented capital efficiency unlocks depeg protection for high yield assets which have been missing from DeFi until the rise of Tapir. 