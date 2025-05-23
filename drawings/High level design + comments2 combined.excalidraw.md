---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==

# High level design combined.excalidraw 1
LRT module ^tfUDXq26

Users ^t1LyL2Gu

Pool
-
receives funds & 
issues LRT for 
the users & allocate to strategies ^4Os68ayP

Strategy A
-
deploys funds in 
restaking 
protocol A, earns 
rewards ^M2Z1WX4e

Deposit ^JaCtNI5u

withdraw ^JQHxmclk

deploy funds ^XfMBwyry

receive funds ^yOBgDnyU

Strategy B
-
deploys funds in 
restaking 
protocol B, earns 
rewards ^YP8fj44E

# Text Elements
LRT module ^tfUDXq26

Users ^t1LyL2Gu

Pool
-
receives funds & 
issues LRT for 
the users & allocate to strategies, keeps track of the LRT share price ^4Os68ayP

Strategy A
-
deploys funds in 
restaking 
protocol A, earns 
rewards ^M2Z1WX4e

Deposit ETH (receive tETH) ^JaCtNI5u

withdraw ETH(send tETH) ^JQHxmclk

deploy funds ^XfMBwyry

receive funds ^yOBgDnyU

Strategy B
-
deploys funds in 
restaking 
protocol B, earns 
rewards ^YP8fj44E

Depeg module
-
receives tETH, mints two partial tokens(0.5DP_tETH+ 0.5YB_tETH), where YB_tETH bares all the depeg risk ^R4d2Arx5

Deposit tETH (receive 0.5 DP_tETH + 0.5 YB_tETH) ^zzYTlPuh

AMM for 
DP_tETH / YB_tETH  ^rI5QapIB

Swap DP_tETH for YB_tETH and vice versa ^NazxEYoF

Fixed yield module
-
receives tETH, mints two tokens(1PT_tETH+ 1YT_tETH), where PT_tETH has fixed yield(implied by its price) and YT_tETH carries all yield
 ^sA7oXaII

Deposit tETH (receive 1 PT_tETH + 1YT_tETH) ^m1X60X9F

AMM for 
PT_tETH / tETH  ^neT5egBB

Swap PT_tETH for tETH and vice versa ^vnpkMnmw

NOTE: 
If user wants DP_tETH, 
they will buy it straight from the pool or mint it
and sell YB_tETH to the pool
IF
user wants YB_tETH, 
they will do the same as above just with reversed tokens.
 

  ^qxNuTBh2

NOTE: 
If user wants PT_tETH, 
they will buy it straight from the pool
IF
user wants YT_tETH, 
they will mint both and sell PT_tETH into the pool
 

  ^YbCFL1G2

Design overview ^k5dB2HEN

tt ^l2o9EoBi

This is a classic pool, that takes 
funds from restakers and issues 
them with LRT token
 ^Ppj8W5Y2

This Depeg module allows users
to buy or sell depeg protection
 ^a6y8LC8m

This Fixed yield module allows 
users to buy a fixed yield product
or purchase just the yield part
 ^G1gQNqhM

Questions / comments ^hX4USqq6

example question 1  ^Jz3NdoAH

%%
# Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.0.18",
	"elements": [
		{
			"type": "rectangle",
			"version": 224,
			"versionNonce": 768789498,
			"isDeleted": false,
			"id": "8IkcJlhJA2zqwbnHVbhLp",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 300,
			"y": 280,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 920,
			"height": 640,
			"seed": 907165252,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "tfUDXq26",
					"type": "text"
				},
				{
					"id": "9BqP7l8p3B1ZwhonG8KfL",
					"type": "arrow"
				},
				{
					"id": "ZXQY-uWiCIlLbTI8nQKKP",
					"type": "arrow"
				}
			],
			"updated": 1727776630747,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 190,
			"versionNonce": 1754217338,
			"isDeleted": false,
			"id": "tfUDXq26",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 709.21875,
			"y": 285,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 101.5625,
			"height": 25,
			"seed": 1426637252,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "LRT module",
			"rawText": "LRT module",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": "8IkcJlhJA2zqwbnHVbhLp",
			"originalText": "LRT module",
			"lineHeight": 1.25,
			"baseline": 19
		},
		{
			"type": "ellipse",
			"version": 242,
			"versionNonce": 397398310,
			"isDeleted": false,
			"id": "7F4kaJTp_7WpER2FSfqmg",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -40,
			"y": 440,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 240,
			"height": 220,
			"seed": 195925700,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "t1LyL2Gu"
				},
				{
					"id": "kSrJfDEEbj0SemHlmwSKp",
					"type": "arrow"
				},
				{
					"id": "Iboz2oIn7Pfch7iKfebWv",
					"type": "arrow"
				},
				{
					"id": "aI9ze98tlK67P0Ek_5NO2",
					"type": "arrow"
				},
				{
					"id": "qvSMzYA-1blZ_3hkkrk-z",
					"type": "arrow"
				},
				{
					"id": "Pv6VPNLQLQoPW-Sbd2UfM",
					"type": "arrow"
				},
				{
					"id": "ZC1fjziGqIVpYHl7kjCl6",
					"type": "arrow"
				}
			],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 103,
			"versionNonce": 1489878074,
			"isDeleted": false,
			"id": "t1LyL2Gu",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 57.2265625,
			"y": 537.5,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 45.546875,
			"height": 25,
			"seed": 68580292,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Users",
			"rawText": "Users",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7F4kaJTp_7WpER2FSfqmg",
			"originalText": "Users",
			"lineHeight": 1.25,
			"baseline": 19
		},
		{
			"type": "rectangle",
			"version": 246,
			"versionNonce": 824622182,
			"isDeleted": false,
			"id": "64h_NGjUVEpl8g2fy5cl0",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 580,
			"y": 360,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 420.00000000000006,
			"height": 219.99999999999997,
			"seed": 2106519420,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "4Os68ayP"
				},
				{
					"id": "Iboz2oIn7Pfch7iKfebWv",
					"type": "arrow"
				},
				{
					"id": "CCAsimPEqxHX4MHRXGzjL",
					"type": "arrow"
				},
				{
					"id": "IdyJ6qxtKZPXwQ7gp8afp",
					"type": "arrow"
				},
				{
					"id": "osWU5rRy9qNaplwaj9c6j",
					"type": "arrow"
				},
				{
					"id": "mUtC2yqqyu3m0H7M42Q8u",
					"type": "arrow"
				},
				{
					"id": "kSrJfDEEbj0SemHlmwSKp",
					"type": "arrow"
				}
			],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 300,
			"versionNonce": 2106546598,
			"isDeleted": false,
			"id": "4Os68ayP",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 599.23828125,
			"y": 395,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 381.5234375,
			"height": 150,
			"seed": 1649019260,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776444631,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Pool\n-\nreceives funds & \nissues LRT for \nthe users & allocate to strategies, keeps track of\nthe LRT share price",
			"rawText": "Pool\n-\nreceives funds & \nissues LRT for \nthe users & allocate to strategies, keeps track of the LRT share price",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "64h_NGjUVEpl8g2fy5cl0",
			"originalText": "Pool\n-\nreceives funds & \nissues LRT for \nthe users & allocate to strategies, keeps track of the LRT share price",
			"lineHeight": 1.25,
			"baseline": 144
		},
		{
			"type": "rectangle",
			"version": 491,
			"versionNonce": 723402662,
			"isDeleted": false,
			"id": "qKrBJ0Le5a2j_7xDAi9Lq",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 440,
			"y": 680,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 187.5,
			"height": 187.5,
			"seed": 388381764,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "M2Z1WX4e"
				},
				{
					"id": "CCAsimPEqxHX4MHRXGzjL",
					"type": "arrow"
				},
				{
					"id": "IdyJ6qxtKZPXwQ7gp8afp",
					"type": "arrow"
				}
			],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 480,
			"versionNonce": 1285780922,
			"isDeleted": false,
			"id": "M2Z1WX4e",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 462.1044921875,
			"y": 698.75,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 143.291015625,
			"height": 150,
			"seed": 857609156,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Strategy A\n-\ndeploys funds in \nrestaking \nprotocol A, earns \nrewards",
			"rawText": "Strategy A\n-\ndeploys funds in \nrestaking \nprotocol A, earns \nrewards",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qKrBJ0Le5a2j_7xDAi9Lq",
			"originalText": "Strategy A\n-\ndeploys funds in \nrestaking \nprotocol A, earns \nrewards",
			"lineHeight": 1.25,
			"baseline": 144
		},
		{
			"type": "arrow",
			"version": 357,
			"versionNonce": 372798586,
			"isDeleted": false,
			"id": "kSrJfDEEbj0SemHlmwSKp",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 210.99945472728385,
			"y": 546.9659121273853,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 349.0005452727162,
			"height": 26.96591212738531,
			"seed": 717628100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "JaCtNI5u"
				}
			],
			"updated": 1727776623596,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			},
			"startBinding": {
				"elementId": "7F4kaJTp_7WpER2FSfqmg",
				"gap": 11.040630159954333,
				"focus": 0.06420622041424785
			},
			"endBinding": {
				"elementId": "64h_NGjUVEpl8g2fy5cl0",
				"gap": 20,
				"focus": -0.2553263708976647
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					349.0005452727162,
					-26.96591212738531
				]
			]
		},
		{
			"type": "text",
			"version": 60,
			"versionNonce": 450932346,
			"isDeleted": false,
			"id": "JaCtNI5u",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 255.62529394803073,
			"y": 494.9846457464888,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 231.572265625,
			"height": 25,
			"seed": 2014652028,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Deposit ETH (receive tETH)",
			"rawText": "Deposit ETH (receive tETH)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kSrJfDEEbj0SemHlmwSKp",
			"originalText": "Deposit ETH (receive tETH)",
			"lineHeight": 1.25,
			"baseline": 19
		},
		{
			"type": "arrow",
			"version": 945,
			"versionNonce": 916423930,
			"isDeleted": false,
			"id": "Iboz2oIn7Pfch7iKfebWv",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 571.6666870117188,
			"y": 444.3151465811526,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 397.28301605095885,
			"height": 19.462560796123284,
			"seed": 718841724,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "JQHxmclk"
				}
			],
			"updated": 1727776623593,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			},
			"startBinding": {
				"elementId": "64h_NGjUVEpl8g2fy5cl0",
				"gap": 8.33331298828125,
				"focus": 0.30244831110702314
			},
			"endBinding": {
				"elementId": "7F4kaJTp_7WpER2FSfqmg",
				"gap": 12.679834850812867,
				"focus": -0.7407476112974124
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-397.28301605095885,
					19.462560796123284
				]
			]
		},
		{
			"type": "text",
			"version": 59,
			"versionNonce": 1182322490,
			"isDeleted": false,
			"id": "JQHxmclk",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 249.18698109089883,
			"y": 445.8300391137233,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 218.828125,
			"height": 25,
			"seed": 208592252,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "withdraw ETH(send tETH)",
			"rawText": "withdraw ETH(send tETH)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Iboz2oIn7Pfch7iKfebWv",
			"originalText": "withdraw ETH(send tETH)",
			"lineHeight": 1.25,
			"baseline": 19
		},
		{
			"type": "arrow",
			"version": 928,
			"versionNonce": 611130874,
			"isDeleted": false,
			"id": "CCAsimPEqxHX4MHRXGzjL",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 665.822726207382,
			"y": 595.0000305175781,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 40.59342175111999,
			"height": 79.58328247070312,
			"seed": 242650948,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "XfMBwyry"
				}
			],
			"updated": 1727776623597,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			},
			"startBinding": {
				"elementId": "64h_NGjUVEpl8g2fy5cl0",
				"gap": 15.000030517578125,
				"focus": 0.22704283405823988
			},
			"endBinding": {
				"elementId": "qKrBJ0Le5a2j_7xDAi9Lq",
				"gap": 5.41668701171875,
				"focus": 0.288882004617076
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-40.59342175111999,
					79.58328247070312
				]
			]
		},
		{
			"type": "text",
			"version": 45,
			"versionNonce": 869193722,
			"isDeleted": false,
			"id": "XfMBwyry",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 583.049192454989,
			"y": 611.6666870117188,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 103.876953125,
			"height": 25,
			"seed": 607001028,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "deploy funds",
			"rawText": "deploy funds",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "CCAsimPEqxHX4MHRXGzjL",
			"originalText": "deploy funds",
			"lineHeight": 1.25,
			"baseline": 19
		},
		{
			"type": "arrow",
			"version": 906,
			"versionNonce": 27617146,
			"isDeleted": false,
			"id": "IdyJ6qxtKZPXwQ7gp8afp",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 634.5833740234375,
			"y": 764.6008532896669,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 131.19064062525229,
			"height": 162.93413576037005,
			"seed": 1685284220,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "yOBgDnyU"
				}
			],
			"updated": 1727776623597,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			},
			"startBinding": {
				"elementId": "qKrBJ0Le5a2j_7xDAi9Lq",
				"gap": 7.0833740234375,
				"focus": 0.5522886414434847
			},
			"endBinding": {
				"elementId": "64h_NGjUVEpl8g2fy5cl0",
				"gap": 21.666717529296875,
				"focus": -0.2739359665413275
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					131.19064062525229,
					-162.93413576037005
				]
			]
		},
		{
			"type": "text",
			"version": 44,
			"versionNonce": 1122355386,
			"isDeleted": false,
			"id": "yOBgDnyU",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 613.8967056274414,
			"y": 651.2363741930449,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 107.16796875,
			"height": 25,
			"seed": 1306630652,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "receive funds",
			"rawText": "receive funds",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "IdyJ6qxtKZPXwQ7gp8afp",
			"originalText": "receive funds",
			"lineHeight": 1.25,
			"baseline": 19
		},
		{
			"type": "rectangle",
			"version": 573,
			"versionNonce": 499365862,
			"isDeleted": false,
			"id": "Lb3z0cDsn7J00jk6QsGnI",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 862.083292643229,
			"y": 686.9298516105446,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 187.5,
			"height": 187.5,
			"seed": 194348356,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "YP8fj44E"
				},
				{
					"id": "osWU5rRy9qNaplwaj9c6j",
					"type": "arrow"
				},
				{
					"id": "mUtC2yqqyu3m0H7M42Q8u",
					"type": "arrow"
				}
			],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 567,
			"versionNonce": 1533059450,
			"isDeleted": false,
			"id": "YP8fj44E",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 884.739542643229,
			"y": 705.6798516105446,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 142.1875,
			"height": 150,
			"seed": 1287404740,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Strategy B\n-\ndeploys funds in \nrestaking \nprotocol B, earns \nrewards",
			"rawText": "Strategy B\n-\ndeploys funds in \nrestaking \nprotocol B, earns \nrewards",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Lb3z0cDsn7J00jk6QsGnI",
			"originalText": "Strategy B\n-\ndeploys funds in \nrestaking \nprotocol B, earns \nrewards",
			"lineHeight": 1.25,
			"baseline": 144
		},
		{
			"type": "arrow",
			"version": 1112,
			"versionNonce": 964251898,
			"isDeleted": false,
			"id": "osWU5rRy9qNaplwaj9c6j",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 848.9639246020131,
			"y": 591.5593851663172,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 64.42943580560768,
			"height": 92.45377943250867,
			"seed": 924845124,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1727776623598,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "64h_NGjUVEpl8g2fy5cl0",
				"gap": 11.559385166317156,
				"focus": 0.08982405752362983
			},
			"endBinding": {
				"elementId": "Lb3z0cDsn7J00jk6QsGnI",
				"gap": 2.91668701171875,
				"focus": 0.1566820154944307
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					64.42943580560768,
					92.45377943250867
				]
			]
		},
		{
			"type": "arrow",
			"version": 1050,
			"versionNonce": 1367399034,
			"isDeleted": false,
			"id": "mUtC2yqqyu3m0H7M42Q8u",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 987.9940103111471,
			"y": 670.7506275805148,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 20.168217865935276,
			"height": 83.25062758051479,
			"seed": 1084152772,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1727776623598,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "Lb3z0cDsn7J00jk6QsGnI",
				"gap": 16.179224030029786,
				"focus": 0.5048185235678117
			},
			"endBinding": {
				"elementId": "64h_NGjUVEpl8g2fy5cl0",
				"gap": 7.5,
				"focus": -0.631148547732798
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-20.168217865935276,
					-83.25062758051479
				]
			]
		},
		{
			"type": "rectangle",
			"version": 324,
			"versionNonce": 284653158,
			"isDeleted": false,
			"id": "OCuA2lA-gUCqjeQMIEepF",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 300,
			"y": 1000,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 380,
			"height": 240.00000000000006,
			"seed": 1452386022,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "R4d2Arx5",
					"type": "text"
				},
				{
					"id": "aI9ze98tlK67P0Ek_5NO2",
					"type": "arrow"
				}
			],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 410,
			"versionNonce": 892209914,
			"isDeleted": false,
			"id": "R4d2Arx5",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 313.5546875,
			"y": 1005,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 352.890625,
			"height": 125,
			"seed": 1757927974,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Depeg module\n-\nreceives tETH, mints two partial\ntokens(0.5DP_tETH+ 0.5YB_tETH), where\nYB_tETH bares all the depeg risk",
			"rawText": "Depeg module\n-\nreceives tETH, mints two partial tokens(0.5DP_tETH+ 0.5YB_tETH), where YB_tETH bares all the depeg risk",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": "OCuA2lA-gUCqjeQMIEepF",
			"originalText": "Depeg module\n-\nreceives tETH, mints two partial tokens(0.5DP_tETH+ 0.5YB_tETH), where YB_tETH bares all the depeg risk",
			"lineHeight": 1.25,
			"baseline": 119
		},
		{
			"type": "arrow",
			"version": 563,
			"versionNonce": 1230242810,
			"isDeleted": false,
			"id": "aI9ze98tlK67P0Ek_5NO2",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 99.03507834345555,
			"y": 678.7927761102744,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 240.77520758598524,
			"height": 302.4603795899641,
			"seed": 93790694,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "zzYTlPuh"
				}
			],
			"updated": 1727776623599,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			},
			"startBinding": {
				"elementId": "7F4kaJTp_7WpER2FSfqmg",
				"gap": 20,
				"focus": 0.562031264833975
			},
			"endBinding": {
				"elementId": "OCuA2lA-gUCqjeQMIEepF",
				"gap": 18.746844299761506,
				"focus": -0.13917981140848487
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					240.77520758598524,
					302.4603795899641
				]
			]
		},
		{
			"type": "text",
			"version": 83,
			"versionNonce": 1474730938,
			"isDeleted": false,
			"id": "zzYTlPuh",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 77.81664132668175,
			"y": 825.6237030747486,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 220.15625,
			"height": 50,
			"seed": 795211046,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Deposit tETH (receive 0.5\nDP_tETH + 0.5 YB_tETH)",
			"rawText": "Deposit tETH (receive 0.5 DP_tETH + 0.5 YB_tETH)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "aI9ze98tlK67P0Ek_5NO2",
			"originalText": "Deposit tETH (receive 0.5 DP_tETH + 0.5 YB_tETH)",
			"lineHeight": 1.25,
			"baseline": 44
		},
		{
			"type": "rectangle",
			"version": 398,
			"versionNonce": 1949144294,
			"isDeleted": false,
			"id": "y1H09hI7Vlj8vYCl1mXpA",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 800,
			"y": 1020,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 440,
			"height": 220.00000000000009,
			"seed": 429715898,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "rI5QapIB",
					"type": "text"
				},
				{
					"id": "qvSMzYA-1blZ_3hkkrk-z",
					"type": "arrow"
				}
			],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 393,
			"versionNonce": 1590629498,
			"isDeleted": false,
			"id": "rI5QapIB",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 928.61328125,
			"y": 1025,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 182.7734375,
			"height": 50,
			"seed": 55224954,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "AMM for \nDP_tETH / YB_tETH ",
			"rawText": "AMM for \nDP_tETH / YB_tETH ",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": "y1H09hI7Vlj8vYCl1mXpA",
			"originalText": "AMM for \nDP_tETH / YB_tETH ",
			"lineHeight": 1.25,
			"baseline": 44
		},
		{
			"type": "arrow",
			"version": 1260,
			"versionNonce": 491606522,
			"isDeleted": false,
			"id": "qvSMzYA-1blZ_3hkkrk-z",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 81.09379297379257,
			"y": 680.9436641765305,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 719.0297950433402,
			"height": 576.9944630265894,
			"seed": 860094458,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "NazxEYoF"
				}
			],
			"updated": 1727776623592,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			},
			"startBinding": {
				"elementId": "7F4kaJTp_7WpER2FSfqmg",
				"gap": 20.947607196291642,
				"focus": 0.3518378504505029
			},
			"endBinding": {
				"elementId": "qxNuTBh2",
				"focus": 0.049293789032348975,
				"gap": 19.87641198286724
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					200.02979504333985,
					576.9944630265894
				],
				[
					719.0297950433402,
					524.9363321115511
				]
			]
		},
		{
			"type": "text",
			"version": 134,
			"versionNonce": 195720506,
			"isDeleted": false,
			"id": "NazxEYoF",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 107.50371497025742,
			"y": 1245.43812720312,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 364.365234375,
			"height": 25,
			"seed": 1769337018,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Swap DP_tETH for YB_tETH and vice versa",
			"rawText": "Swap DP_tETH for YB_tETH and vice versa",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qvSMzYA-1blZ_3hkkrk-z",
			"originalText": "Swap DP_tETH for YB_tETH and vice versa",
			"lineHeight": 1.25,
			"baseline": 19
		},
		{
			"type": "rectangle",
			"version": 360,
			"versionNonce": 843977574,
			"isDeleted": false,
			"id": "tGq6v-UEsBS5_yOaI2T56",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 300.01148168572456,
			"y": 1381.4542240902786,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 380,
			"height": 240.00000000000006,
			"seed": 2044426918,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "sA7oXaII",
					"type": "text"
				},
				{
					"id": "ZC1fjziGqIVpYHl7kjCl6",
					"type": "arrow"
				}
			],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 408,
			"versionNonce": 1876671994,
			"isDeleted": false,
			"id": "sA7oXaII",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 306.34937231072456,
			"y": 1386.4542240902786,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 367.32421875,
			"height": 175,
			"seed": 1931556326,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Fixed yield module\n-\nreceives tETH, mints two tokens(1PT_tETH+\n1YT_tETH), where PT_tETH has fixed\nyield(implied by its price) and YT_tETH\ncarries all yield\n",
			"rawText": "Fixed yield module\n-\nreceives tETH, mints two tokens(1PT_tETH+ 1YT_tETH), where PT_tETH has fixed yield(implied by its price) and YT_tETH carries all yield\n",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": "tGq6v-UEsBS5_yOaI2T56",
			"originalText": "Fixed yield module\n-\nreceives tETH, mints two tokens(1PT_tETH+ 1YT_tETH), where PT_tETH has fixed yield(implied by its price) and YT_tETH carries all yield\n",
			"lineHeight": 1.25,
			"baseline": 169
		},
		{
			"type": "arrow",
			"version": 759,
			"versionNonce": 1189442746,
			"isDeleted": false,
			"id": "ZC1fjziGqIVpYHl7kjCl6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -20.001852643733088,
			"y": 619.9902074545537,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 319.0133343294576,
			"height": 859.3507803359294,
			"seed": 177047846,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "m1X60X9F"
				}
			],
			"updated": 1727776623601,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			},
			"startBinding": {
				"elementId": "7F4kaJTp_7WpER2FSfqmg",
				"gap": 5.63013396087689,
				"focus": 0.9298148655192312
			},
			"endBinding": {
				"elementId": "tGq6v-UEsBS5_yOaI2T56",
				"gap": 1,
				"focus": -0.4265679609467748
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					140.0018526437331,
					740.0097925454463
				],
				[
					319.0133343294576,
					859.3507803359294
				]
			]
		},
		{
			"type": "text",
			"version": 98,
			"versionNonce": 2019946170,
			"isDeleted": false,
			"id": "m1X60X9F",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 24.9400634765625,
			"y": 1335,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 196.806640625,
			"height": 50,
			"seed": 1871541350,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Deposit tETH (receive 1\nPT_tETH + 1YT_tETH)",
			"rawText": "Deposit tETH (receive 1 PT_tETH + 1YT_tETH)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ZC1fjziGqIVpYHl7kjCl6",
			"originalText": "Deposit tETH (receive 1 PT_tETH + 1YT_tETH)",
			"lineHeight": 1.25,
			"baseline": 44
		},
		{
			"type": "rectangle",
			"version": 430,
			"versionNonce": 474018278,
			"isDeleted": false,
			"id": "8DuEHyHFag6R5BAMChoFo",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 800.0114816857244,
			"y": 1401.4542240902786,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 439.9885183142755,
			"height": 220.00000000000009,
			"seed": 1542322086,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "neT5egBB",
					"type": "text"
				},
				{
					"id": "Pv6VPNLQLQoPW-Sbd2UfM",
					"type": "arrow"
				}
			],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 416,
			"versionNonce": 2045511546,
			"isDeleted": false,
			"id": "neT5egBB",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 948.6239049053622,
			"y": 1406.4542240902786,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 142.763671875,
			"height": 50,
			"seed": 1205605094,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "AMM for \nPT_tETH / tETH ",
			"rawText": "AMM for \nPT_tETH / tETH ",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": "8DuEHyHFag6R5BAMChoFo",
			"originalText": "AMM for \nPT_tETH / tETH ",
			"lineHeight": 1.25,
			"baseline": 44
		},
		{
			"type": "arrow",
			"version": 1273,
			"versionNonce": 445304186,
			"isDeleted": false,
			"id": "Pv6VPNLQLQoPW-Sbd2UfM",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -60.007576732807706,
			"y": 579.9536977439532,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 859.0190584185322,
			"height": 1100.0463022560468,
			"seed": 501532198,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "vnpkMnmw"
				}
			],
			"updated": 1727776623602,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			},
			"startBinding": {
				"elementId": "7F4kaJTp_7WpER2FSfqmg",
				"gap": 23.661480141361338,
				"focus": 1.194215565509141
			},
			"endBinding": {
				"elementId": "8DuEHyHFag6R5BAMChoFo",
				"gap": 1,
				"focus": -0.27662296398490344
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					180.0075767328077,
					1100.0463022560468
				],
				[
					859.0190584185322,
					1002.4430292691256
				]
			]
		},
		{
			"type": "text",
			"version": 133,
			"versionNonce": 1018234938,
			"isDeleted": false,
			"id": "vnpkMnmw",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 122.97159521111524,
			"y": 1628.9542240902786,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 324.35546875,
			"height": 25,
			"seed": 1861554534,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Swap PT_tETH for tETH and vice versa",
			"rawText": "Swap PT_tETH for tETH and vice versa",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Pv6VPNLQLQoPW-Sbd2UfM",
			"originalText": "Swap PT_tETH for tETH and vice versa",
			"lineHeight": 1.25,
			"baseline": 19
		},
		{
			"type": "text",
			"version": 509,
			"versionNonce": 1760440422,
			"isDeleted": false,
			"id": "qxNuTBh2",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 820,
			"y": 1100,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 411.5174560546875,
			"height": 177.26840733957198,
			"seed": 1646869158,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "qvSMzYA-1blZ_3hkkrk-z",
					"type": "arrow"
				}
			],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 14.181472587165757,
			"fontFamily": 1,
			"text": "NOTE: \nIf user wants DP_tETH, \nthey will buy it straight from the pool or mint it\nand sell YB_tETH to the pool\nIF\nuser wants YB_tETH, \nthey will do the same as above just with reversed tokens.\n \n\n ",
			"rawText": "NOTE: \nIf user wants DP_tETH, \nthey will buy it straight from the pool or mint it\nand sell YB_tETH to the pool\nIF\nuser wants YB_tETH, \nthey will do the same as above just with reversed tokens.\n \n\n ",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "NOTE: \nIf user wants DP_tETH, \nthey will buy it straight from the pool or mint it\nand sell YB_tETH to the pool\nIF\nuser wants YB_tETH, \nthey will do the same as above just with reversed tokens.\n \n\n ",
			"lineHeight": 1.25,
			"baseline": 171
		},
		{
			"type": "text",
			"version": 335,
			"versionNonce": 144175354,
			"isDeleted": false,
			"id": "YbCFL1G2",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 820,
			"y": 1460,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 360.35601806640625,
			"height": 159.54156660561478,
			"seed": 931844730,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432056,
			"link": null,
			"locked": false,
			"fontSize": 14.181472587165757,
			"fontFamily": 1,
			"text": "NOTE: \nIf user wants PT_tETH, \nthey will buy it straight from the pool\nIF\nuser wants YT_tETH, \nthey will mint both and sell PT_tETH into the pool\n \n\n ",
			"rawText": "NOTE: \nIf user wants PT_tETH, \nthey will buy it straight from the pool\nIF\nuser wants YT_tETH, \nthey will mint both and sell PT_tETH into the pool\n \n\n ",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "NOTE: \nIf user wants PT_tETH, \nthey will buy it straight from the pool\nIF\nuser wants YT_tETH, \nthey will mint both and sell PT_tETH into the pool\n \n\n ",
			"lineHeight": 1.25,
			"baseline": 154
		},
		{
			"type": "rectangle",
			"version": 40,
			"versionNonce": 1184607910,
			"isDeleted": false,
			"id": "1ahwZeJhHre__tt8_WKf7",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 260,
			"y": 960,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 999.9999999999999,
			"height": 320,
			"seed": 975592934,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "H_QqumIsicNgPkjItYpOJ",
					"type": "arrow"
				}
			],
			"updated": 1727776458981,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 54,
			"versionNonce": 583715578,
			"isDeleted": false,
			"id": "e5b5UBy5-n8EaCLc2mnA0",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 260,
			"y": 1360,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 999.9999999999999,
			"height": 320,
			"seed": 1264312634,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "FN8NlTWn-Lv98k5waENEE",
					"type": "arrow"
				}
			],
			"updated": 1727776450462,
			"link": null,
			"locked": false
		},
		{
			"type": "arrow",
			"version": 28,
			"versionNonce": 676912314,
			"isDeleted": false,
			"id": "9BqP7l8p3B1ZwhonG8KfL",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1240,
			"y": 500,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 120,
			"height": 0,
			"seed": 689903674,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1727776623590,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "8IkcJlhJA2zqwbnHVbhLp",
				"gap": 20,
				"focus": -0.3125
			},
			"endBinding": {
				"elementId": "Ppj8W5Y2",
				"gap": 20,
				"focus": 0.2
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					120,
					0
				]
			]
		},
		{
			"type": "text",
			"version": 7,
			"versionNonce": 1750473530,
			"isDeleted": false,
			"id": "l2o9EoBi",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 828.7000122070312,
			"y": 937.5,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 22.5999755859375,
			"height": 25,
			"seed": 1629572710,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776432057,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "tt",
			"rawText": "tt",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": null,
			"originalText": "tt",
			"lineHeight": 1.25,
			"baseline": 17
		},
		{
			"type": "text",
			"version": 141,
			"versionNonce": 68668774,
			"isDeleted": false,
			"id": "Ppj8W5Y2",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1380,
			"y": 460,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 348.979736328125,
			"height": 100,
			"seed": 1313710650,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "9BqP7l8p3B1ZwhonG8KfL",
					"type": "arrow"
				}
			],
			"updated": 1727776432057,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "This is a classic pool, that takes \nfunds from restakers and issues \nthem with LRT token\n",
			"rawText": "This is a classic pool, that takes \nfunds from restakers and issues \nthem with LRT token\n",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "This is a classic pool, that takes \nfunds from restakers and issues \nthem with LRT token\n",
			"lineHeight": 1.25,
			"baseline": 92
		},
		{
			"type": "rectangle",
			"version": 190,
			"versionNonce": 647008762,
			"isDeleted": false,
			"id": "M1wW99p-50WJNfIcbwSZR",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -140,
			"y": 80,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1960,
			"height": 1700,
			"seed": 390883302,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "k5dB2HEN"
				}
			],
			"updated": 1727776544983,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 156,
			"versionNonce": 307909094,
			"isDeleted": false,
			"id": "k5dB2HEN",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 764.9100723266602,
			"y": 85,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 150.1798553466797,
			"height": 25,
			"seed": 2139007974,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776560666,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Design overview",
			"rawText": "Design overview",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": "M1wW99p-50WJNfIcbwSZR",
			"originalText": "Design overview",
			"lineHeight": 1.25,
			"baseline": 17
		},
		{
			"type": "arrow",
			"version": 220,
			"versionNonce": 1460436006,
			"isDeleted": false,
			"id": "H_QqumIsicNgPkjItYpOJ",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1280.7557503275575,
			"y": 1093.121916260515,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 119.99999999999977,
			"height": 1.4151082920461704,
			"seed": 982759098,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1727776483364,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "1ahwZeJhHre__tt8_WKf7",
				"focus": -0.125,
				"gap": 20.75575032755728
			},
			"endBinding": {
				"elementId": "a6y8LC8m",
				"focus": 0.2,
				"gap": 20
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					119.99999999999977,
					-1.4151082920461704
				]
			]
		},
		{
			"type": "text",
			"version": 213,
			"versionNonce": 1986735526,
			"isDeleted": false,
			"id": "a6y8LC8m",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1420.7557503275573,
			"y": 1060,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 311.8397216796875,
			"height": 75,
			"seed": 1126223738,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "H_QqumIsicNgPkjItYpOJ",
					"type": "arrow"
				}
			],
			"updated": 1727776483363,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "This Depeg module allows users\nto buy or sell depeg protection\n",
			"rawText": "This Depeg module allows users\nto buy or sell depeg protection\n",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "This Depeg module allows users\nto buy or sell depeg protection\n",
			"lineHeight": 1.25,
			"baseline": 67
		},
		{
			"type": "arrow",
			"version": 274,
			"versionNonce": 818127910,
			"isDeleted": false,
			"id": "FN8NlTWn-Lv98k5waENEE",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1281.0445643492044,
			"y": 1519.9999999947154,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 120,
			"height": 1.8376340449322015e-9,
			"seed": 1123114790,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1727776528809,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "e5b5UBy5-n8EaCLc2mnA0",
				"focus": 0,
				"gap": 21.044564349204393
			},
			"endBinding": {
				"elementId": "G1gQNqhM",
				"focus": 0.2,
				"gap": 20
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					120,
					1.8376340449322015e-9
				]
			]
		},
		{
			"type": "text",
			"version": 251,
			"versionNonce": 1212962214,
			"isDeleted": false,
			"id": "G1gQNqhM",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1421.0445643492044,
			"y": 1480,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 341.85968017578125,
			"height": 100,
			"seed": 1493600870,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "FN8NlTWn-Lv98k5waENEE",
					"type": "arrow"
				}
			],
			"updated": 1727776528808,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "This Fixed yield module allows \nusers to buy a fixed yield product\nor purchase just the yield part\n",
			"rawText": "This Fixed yield module allows \nusers to buy a fixed yield product\nor purchase just the yield part\n",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "This Fixed yield module allows \nusers to buy a fixed yield product\nor purchase just the yield part\n",
			"lineHeight": 1.25,
			"baseline": 92
		},
		{
			"type": "rectangle",
			"version": 69,
			"versionNonce": 1775725414,
			"isDeleted": false,
			"id": "5uX10kCp0ciDXHgyhVEpU",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 320,
			"y": -320,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1000,
			"height": 320,
			"seed": 1479441702,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1727776630125,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 43,
			"versionNonce": 132189862,
			"isDeleted": false,
			"id": "hX4USqq6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 700,
			"y": -300,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 213.0998077392578,
			"height": 25,
			"seed": 1156573286,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727776630125,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Questions / comments",
			"rawText": "Questions / comments",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Questions / comments",
			"lineHeight": 1.25,
			"baseline": 17
		},
		{
			"type": "text",
			"version": 78,
			"versionNonce": 1331882426,
			"isDeleted": false,
			"id": "Jz3NdoAH",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 360,
			"y": -240,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 189.83984375,
			"height": 25,
			"seed": 1155656614,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "ZXQY-uWiCIlLbTI8nQKKP",
					"type": "arrow"
				}
			],
			"updated": 1727776630747,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "example question 1 ",
			"rawText": "example question 1 ",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "example question 1 ",
			"lineHeight": 1.25,
			"baseline": 17
		},
		{
			"type": "arrow",
			"version": 168,
			"versionNonce": 250299194,
			"isDeleted": false,
			"id": "ZXQY-uWiCIlLbTI8nQKKP",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 500,
			"y": -200,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 60,
			"height": 460,
			"seed": 1446086374,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1727776630747,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "Jz3NdoAH",
				"focus": -0.5040585693466095,
				"gap": 15
			},
			"endBinding": {
				"elementId": "8IkcJlhJA2zqwbnHVbhLp",
				"focus": -0.7261698440207972,
				"gap": 20
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-60,
					460
				]
			]
		}
	],
	"appState": {
		"theme": "light",
		"viewBackgroundColor": "#ffffff",
		"currentItemStrokeColor": "#1e1e1e",
		"currentItemBackgroundColor": "transparent",
		"currentItemFillStyle": "solid",
		"currentItemStrokeWidth": 0.5,
		"currentItemStrokeStyle": "dashed",
		"currentItemRoughness": 1,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 1,
		"currentItemFontSize": 20,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": 299.73388671875,
		"scrollY": 572.2222222222222,
		"zoom": {
			"value": 0.45
		},
		"currentItemRoundness": "round",
		"gridSize": 20,
		"gridColor": {
			"Bold": "#C9C9C9FF",
			"Regular": "#EDEDEDFF"
		},
		"currentStrokeOptions": null,
		"previousGridSize": null,
		"frameRendering": {
			"enabled": true,
			"clip": true,
			"name": true,
			"outline": true
		}
	},
	"files": {}
}
```
%%