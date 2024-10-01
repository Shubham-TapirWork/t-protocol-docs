# Tapir protocol litepaper

- [Overview](#Overview)
- [USP - unique selling proposition](#USP%20-%20unique%20selling%20proposition)
	- [Go to Market](#Go%20to%20Market)
	- [Token incentives](#Token%20incentives)
- [High level system design](#High%20level%20system%20design)
- [Modules](#Modules)
	- [LRT module](#LRT%20module)
	- [Depeg protection module](#Depeg%20protection%20module)
		- [What makes this depeg protection unique?](#What%20makes%20this%20depeg%20protection%20unique?)
		- [Schematic outline](#Schematic%20outline)
		- [Unlocks](#Unlocks)
		- [Example](#Example)
			- [With depeg event](#With%20depeg%20event)
			- [With NO depeg event](#With%20NO%20depeg%20event)
		- [User incentives](#User%20incentives)
	- [Fixed yield module](#Fixed%20yield%20module)
		- [Why to make this module?](#Why%20to%20make%20this%20module?)
		- [Schematic outline](#Schematic%20outline)
		- [Unlocks](#Unlocks)
		- [Example](#Example)
- [Takeaways](#Takeaways)
	- [Why should investors care about another LRT?](#Why%20should%20investors%20care%20about%20another%20LRT?)
	- [What makes this LRT unique](#What%20makes%20this%20LRT%20unique)


## Overview

Tapir protocol is an native LRT with **LRT wih tunable risk & yield.**

The depeg protection module allows for protecting risk averse investors against slashing risk unlocking much higher yield than regular ETH staking rewards without the risks of restaking. It also enables sophisticated investors who can estimate restaking risks to boost their yield by selling this protection.

Fixed yield is a preferred vehicle for many investors, as seen in traditional markets It also allows for a leveraged long yield strategy which sophisticated investors can leverage to earn multiples of restaking yield.

## USP - unique selling proposition

**Investors can buy protection against slashing**
Restakers will have the ability to either sell or purchase depeg protection, which will either boost their yield or allow them to sleep easier by protecting themselves against depeg events.

This solves the main pain-point that restaking investors are now facing. Every staker would rather have higher restaking yields, but not many become restakers since it is hard to reason about the heterogeneous risk that restaking brings. With tapir they will be able to enjoy restaking yields with safety characteristics of staking. 

**Investors can further boost their yield**
Investors can further increase their yield by selling depeg protection.

**Investors can have a fixed yield**
Restakers can purchase only fixed yield part of the product which is a preferred vehicle for many investors, as seen in traditional markets.

**Investors can have a leveraged long yield**
The more sophisticated investors can earn multiples of restaking yield.



### Go to Market

> [!internal] ?maybe expand this section?

The first target audience(TA) are restakers in Nektar ecosystem. There is a close connection between founders of both projects.
The plan is to first launch the LRT on nectar, where it will be one of the very first LRTs to launch and become the dominant player in this ecosystem and then move to other ones.

Also, the DVT technology that Nektar leverages on its platform further derisks restakers. This creates a natural symbiosis of risk aware LRT protocol and risk minimised restaking platform. 

The next market to capture will be other smaller restaking platform (Karak / Symbiotic) before putting our BD resources into Eigenlayer.

### Token incentives

The strategy is to employ token incentives for aggressive growth. The protocol will reward its early adopters with its protocol token. These rewards will be allocated to both early stakers bringing necessary capital to bootstrap the project. There will be concrete targets of PCV(protocol controlled value) to be reached within each incentivization round. This will have an effect of redistributing the token to its early stakeholders, while a lockup period may be employed to prevent automated token farming and ensure long-term incentive alignment with the protocol.

Have a concrete PCV targets based on which it regulates the token issuance and not overpay for growth. 

Larger size helps the protocol to be more capital efficient as well as being considered a collateral in other DeFi protocols.

Targets:

- Quickly reaching the PCV target
- Make stakeholders & protocol evangelists out of early adopters

The strategy is to track these outcomes and and create a closed loop that will control the protocol inflation and prevent overpaying

## High level system design

Here is a design schema, all modules are explained in detail below.

![[High level design combined.excalidraw | 1400]]

## Modules

The protocol consists of a basic pooling module that gathers & allocates funds and two other modules responsible for the unique properties of the protocol. 
Those are the depeg protection & fixed yield modules. 

### LRT module

This is a module that pools funds from restaker and mints LRTs in their stead. It then allocates the funds to strategies, which in our case will be deployment in different restaking networks. 
This module is similar to what competition offers.


### Depeg protection module

#### What makes this depeg protection unique?

There are multiple ways how investors can insure their depeg protection. They could purchase insurance products, or options and other derivatives. However, no other depeg protection mechanisms carries 100% yield of the underlying asset. With insurance products & options their are denominated in non-productive asset(USD, ETH). This module is unique since it is the most capital efficient at the given amount of protection. Since the protection is purchased in the underlying asset and not in ETH/USD there is no "dead" capital as with other similar products.

#### Schematic outline

![[Depeg Protection module 2024-08-26 11.22.21.excalidraw| 1000]]

![https://i.imgur.com/8FUTaBB.png](https://i.imgur.com/8FUTaBB.png)

#### Unlocks

This module unlocks these yield strategies & their combination:

- **derisking investment** by purchasing depeg protection
- **boosting yield** by selling depeg protection and taking on additional risk

#### Example

**Assumption** We assume that the maturity period is **1 year** in this calculation, for sake of greater clarity, however, the actual maturity could be different.

split - 1 tETH => 0.5DP + 0.5YB

- In this step Alice splits tETH into 0.5DP_ tETH and 0.5YB_ tETH
    - derisking investment
        - If she wants depeg protection she will sell the yield boosted part (0.5YB_ tETH) for depeg protected part (DP_ tETH).
        - Let's assume the price for YB_ tETH is 1.02 YB_ tETH/DP_ tETH. Thus by selling 0.5YB_ tETH, she will be able to get 0.49DP_ tETH(0.5/1.02). Thus Alice's initial position of 1 tETH will translate into 0.99DP_ tETH(0.5minted+0.49bought).
    - boosting yield
        - Conversely Bob based on his calculations believes that the risk adjusted return of selling the depeg protection is warranted and he is willing to take the other side of the trade that Alice is making. Thus Bob's initial position of 1 tETH will translate into 1.01YB_ tETH(0.5minted+0.51bought).

##### With depeg event

Let's assume 5% depeg of the tETH at expiry, let's continue with Alice's & Bob's position from the previous example.

Alice holds 0.99DP_ tETH. Holding a DP token entitles her to redeem her depeg protection token one to one at expiry. Hence she can redeem 0.99DP_ tETH for 0.99 tETH. The pool holding the tETH will redeem 100% of DP_ tETH and 90% YB_ tETH(1-2x(0.05)).

Alice will receive her full amount of PT tokens she is entitled to by her position of 0.99DP_ tETH. If we were to assume that the implied yield of tETH is 7% her effective profit is ~5.9%(1.07x0.99x1). It is important to note that she can lock in this profit at the time of purchasing the depeg protection. The only caveat is that the depeg event must be less or equal to 50%. (This is implied by the structure of the token split). Thus her cost of insurance is ~1%.

On the other hand Bob receives 101% of the fixed profit of PT token but he is also exposed to double the depeg risk since his YB token covers the depeg loss for Alice's DP token. If we assume that the implied yield of tETH is 7% his effective loss is ~2.7%(1.07x1.01x0.9-1).

##### With NO depeg event

Bob's position under no depeg event translates into ~8%(1.07x1.01x1) yield, meaning his yield is boosted by 1%, while Alice's position(0.99DP_ tETH) translates into the same ~5.9%(1.07x0.99x1).

**NOTE** Note that there is no "dead"(undeployed) capital in the system. Both Alice and Bob are fully exposed to the underlying.

#### User incentives

**YT_tETH buyer** this user believes the future tETH yield will be higher than the expected yield implied by YT_tETH price. Also, there is an implied premium with taking on variable yield and selling the fixed part.

**tETH buyer** this user believes the future tETH yield will be lower than the expected yield implied by YT_tETH price. Alternatively he may be willing to pay premium for fixing his yield.

**DP_ tETH buyer** this user wants as safe yield profile as possible. This product allows him to both fix the future restaking yield as well as protect against depeg event. He is willing to pay for this in terms of decreased yield.

**YB_ tETH buyer** this user is looking for the highest fixed yield possible. He does not believe that tETH depeg is likely and is willing sell the DP_ tETH in order to boost yields.

### Fixed yield module

#### Why to make this module?

The more conservative investors prefer to remove variability from their yield and fix it. On the other hand the more sophisticated ones may prefer to leverage their yield, by selling the fixed part and buy the variable one. It can also be used as a tool for selling & purchasing points and an airdrop associated with them. As we have seen, this proved very [oblubeny] feature in the past few months

There are other protocols with this feature, however it is quite advantageous to integrate it directly into the core protocol as this removes any external dependencies on the third parties & allows us to tailor it specifically to our use case.

#### Schematic outline

![[Fixed yield module 2024-08-26 11.22.21.excalidraw| 1000]]

![ | 1000](https://i.imgur.com/tR2uqjg.png)


#### Unlocks

This module unlocks these yield strategies & their combination:

- **fixing yield** by keeping only PT token thus decreasing yield volatility
- **leveraged long yield**, by buying only YT tokens. A high risk strategy that could carry large yields
- **liquidity provisioning** in the fixed yield AMM. This could be done in a yield neutral way(keeping proportional LP+YT exposure) or more geared towards fixed yield (keeping LP only).

#### Example

split - 1 tETH => 1PT +1YT

- fixing yield
    - Alice wants to fix her yield thus she will purchase 1PT_tETH for her tETH. Alternatively she could split her tETH and sell the YT token for PT at later date if she thinks the price will be more favorable.
- leveraged long yield
    - Bob believes that tETH's yield will be higher than YT_tETH's price implies. If he is right he can have a high leverage on this trade by just purchasing YT_tETH for his tETH.
- liquidity provisioning
    - Charlie believes that many users will want to trade this fixed yield, thus he wants to earn the trading fees and provide liquidity.
    - Thus he will sell portion of his tETH for PT_tETH which he needs in order to become LP. His effective position is having some part of his yield fixed while some part not. Both of these tokens carry yield, but under certain conditions it might be more beneficial to own just one of them.

## Takeaways

### Why should investors care about another LRT?

LRTs offer a new unique opportunity and uncap the yield potential. New apps can leverage the security of ETH. This is a good news for an investor, but now the risk profile becomes very heterogeneous and hard to reason about. Depeg protection addresses this main problem restaking faces, by allowing sophisticated players to take on the risk.

This will allow for larger gains than vanilla staking but without the risks of restaking.

### What makes this LRT unique?

As investing 101 tells us, yield & risk come together. Incorporating these special modules in the LRT allows investors to express their investment preferences in much more nuanced ways.

**Express risk & yield preferences** They can take either on _more_ yield & risk or _less_ of both. They can also fix their yield or not. These more nuanced preferences allow for more sophisticated investors that have been on the sidelines till now to come enter the LRT market.

_Note_ that these modules can mix and match. e.g. Risk averse investor may prefer to both fix their yield while purchasing depeg protection.