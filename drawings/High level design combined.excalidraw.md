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
the users & allocate to strategies ^4Os68ayP

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

Depeg module ^R4d2Arx5

Deposit tETH (receive 0.5 DP_tETH + 0.5 YB_tETH) ^zzYTlPuh

AMM for 
DP_tETH / YB_tETH  ^rI5QapIB

Swap DP_tETH for YB_tETH and vice versa ^NazxEYoF

Questions / comments ^RwpTObWy

example question 1  ^AZBIG8gE

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
			"version": 205,
			"versionNonce": 1932048678,
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
				}
			],
			"updated": 1727690524303,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 169,
			"versionNonce": 2011220154,
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
			"updated": 1727690504445,
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
			"version": 220,
			"versionNonce": 167294950,
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
				}
			],
			"updated": 1727690504445,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 82,
			"versionNonce": 956014970,
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
			"updated": 1727690504445,
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
			"version": 173,
			"versionNonce": 522504998,
			"isDeleted": false,
			"id": "64h_NGjUVEpl8g2fy5cl0",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 650,
			"y": 397.9166564941406,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 187.5,
			"height": 187.5,
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
				}
			],
			"updated": 1727690504445,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 110,
			"versionNonce": 1790796346,
			"isDeleted": false,
			"id": "4Os68ayP",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 664.6142578125,
			"y": 416.6666564941406,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 158.271484375,
			"height": 150,
			"seed": 1649019260,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727690504445,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Pool\n-\nreceives funds & \nissues LRT for \nthe users & allocate\nto strategies",
			"rawText": "Pool\n-\nreceives funds & \nissues LRT for \nthe users & allocate to strategies",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "64h_NGjUVEpl8g2fy5cl0",
			"originalText": "Pool\n-\nreceives funds & \nissues LRT for \nthe users & allocate to strategies",
			"lineHeight": 1.25,
			"baseline": 144
		},
		{
			"type": "rectangle",
			"version": 466,
			"versionNonce": 871134822,
			"isDeleted": false,
			"id": "qKrBJ0Le5a2j_7xDAi9Lq",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 413.6573282877604,
			"y": 680.1852484809027,
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
			"updated": 1727690504445,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 451,
			"versionNonce": 671681274,
			"isDeleted": false,
			"id": "M2Z1WX4e",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 435.7618204752604,
			"y": 698.9352484809027,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 143.291015625,
			"height": 150,
			"seed": 857609156,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727690504445,
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
			"version": 303,
			"versionNonce": 18659750,
			"isDeleted": false,
			"id": "kSrJfDEEbj0SemHlmwSKp",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 210.9994805012542,
			"y": 546.965910135931,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 440.53699034016586,
			"height": 31.958423752754186,
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
			"updated": 1727690504445,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			},
			"startBinding": {
				"elementId": "7F4kaJTp_7WpER2FSfqmg",
				"gap": 11.040655978529095,
				"focus": 0.058627319032556614
			},
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					440.53699034016586,
					-31.958423752754186
				]
			]
		},
		{
			"type": "text",
			"version": 39,
			"versionNonce": 929143738,
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
			"width": 221.1398468017578,
			"height": 25,
			"seed": 2014652028,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727690504445,
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
			"version": 362,
			"versionNonce": 501388518,
			"isDeleted": false,
			"id": "Iboz2oIn7Pfch7iKfebWv",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 641.6666870117188,
			"y": 463.91579157961337,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 463.2638349775672,
			"height": 3.7930344406954646,
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
			"updated": 1727690504445,
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
					-463.2638349775672,
					3.7930344406954646
				]
			]
		},
		{
			"type": "text",
			"version": 39,
			"versionNonce": 384439418,
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
			"width": 212.81982421875,
			"height": 25,
			"seed": 208592252,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727690504445,
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
			"version": 243,
			"versionNonce": 868943910,
			"isDeleted": false,
			"id": "CCAsimPEqxHX4MHRXGzjL",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 648.5751456046546,
			"y": 600.3488601319277,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 43.35327809679552,
			"height": 76.25588292219493,
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
			"updated": 1727690504445,
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
					-43.35327809679552,
					76.25588292219493
				]
			]
		},
		{
			"type": "text",
			"version": 25,
			"versionNonce": 140866874,
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
			"width": 107.5399169921875,
			"height": 25,
			"seed": 607001028,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727690504445,
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
			"version": 221,
			"versionNonce": 851645286,
			"isDeleted": false,
			"id": "IdyJ6qxtKZPXwQ7gp8afp",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 608.2407023111979,
			"y": 753.7626446971888,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 100.00803271502843,
			"height": 146.67927067375126,
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
			"updated": 1727690504445,
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
					100.00803271502843,
					-146.67927067375126
				]
			]
		},
		{
			"type": "text",
			"version": 24,
			"versionNonce": 490126842,
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
			"width": 109.45991516113281,
			"height": 25,
			"seed": 1306630652,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727690504445,
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
			"version": 556,
			"versionNonce": 85440166,
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
			"updated": 1727690504445,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 546,
			"versionNonce": 1113648826,
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
			"updated": 1727690504445,
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
			"version": 529,
			"versionNonce": 1131803110,
			"isDeleted": false,
			"id": "osWU5rRy9qNaplwaj9c6j",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 821.027426647518,
			"y": 596.9760416604578,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 76.98492825005587,
			"height": 87.03712293836804,
			"seed": 924845124,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1727690504445,
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
					76.98492825005587,
					87.03712293836804
				]
			]
		},
		{
			"type": "arrow",
			"version": 467,
			"versionNonce": 1283917690,
			"isDeleted": false,
			"id": "mUtC2yqqyu3m0H7M42Q8u",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 961.4939616643342,
			"y": 670.7506275805148,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 116.49396166433417,
			"height": 175.02999920692469,
			"seed": 1084152772,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1727690504445,
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
					-116.49396166433417,
					-175.02999920692469
				]
			]
		},
		{
			"type": "rectangle",
			"version": 305,
			"versionNonce": 1078934202,
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
			"updated": 1727690522155,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 255,
			"versionNonce": 65800250,
			"isDeleted": false,
			"id": "R4d2Arx5",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 431.40625,
			"y": 1005,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 117.1875,
			"height": 25,
			"seed": 1757927974,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727690504445,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Depeg module",
			"rawText": "Depeg module",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": "OCuA2lA-gUCqjeQMIEepF",
			"originalText": "Depeg module",
			"lineHeight": 1.25,
			"baseline": 19
		},
		{
			"type": "arrow",
			"version": 472,
			"versionNonce": 115552358,
			"isDeleted": false,
			"id": "aI9ze98tlK67P0Ek_5NO2",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 99.04393069456663,
			"y": 678.7916477304702,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 240.76966530938782,
			"height": 302.46150796976826,
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
			"updated": 1727690504445,
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
					240.76966530938782,
					302.46150796976826
				]
			]
		},
		{
			"type": "text",
			"version": 64,
			"versionNonce": 812839162,
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
			"width": 205.619873046875,
			"height": 50,
			"seed": 795211046,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727690504445,
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
			"version": 339,
			"versionNonce": 2071758694,
			"isDeleted": false,
			"id": "y1H09hI7Vlj8vYCl1mXpA",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 300,
			"y": 1280,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 380,
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
			"updated": 1727690518491,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 321,
			"versionNonce": 631161274,
			"isDeleted": false,
			"id": "rI5QapIB",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 398.61328125,
			"y": 1285,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 182.7734375,
			"height": 50,
			"seed": 55224954,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727690504446,
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
			"version": 452,
			"versionNonce": 435343078,
			"isDeleted": false,
			"id": "qvSMzYA-1blZ_3hkkrk-z",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1.0937942795455342,
			"y": 660.9436679430306,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 298.90620572045447,
			"height": 739.0563320569694,
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
			"updated": 1727690504446,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			},
			"startBinding": {
				"elementId": "7F4kaJTp_7WpER2FSfqmg",
				"focus": 0.9671449806388879,
				"gap": 23.005543629442286
			},
			"endBinding": {
				"elementId": "y1H09hI7Vlj8vYCl1mXpA",
				"focus": -0.827521326926954,
				"gap": 1
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
					298.90620572045447,
					739.0563320569694
				]
			]
		},
		{
			"type": "text",
			"version": 104,
			"versionNonce": 1318222458,
			"isDeleted": false,
			"id": "NazxEYoF",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 54.40696641467511,
			"y": 1005.4718339715153,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 192.2798614501953,
			"height": 50,
			"seed": 1769337018,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727690504446,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Swap DP_tETH for\nYB_tETH and vice versa",
			"rawText": "Swap DP_tETH for YB_tETH and vice versa",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qvSMzYA-1blZ_3hkkrk-z",
			"originalText": "Swap DP_tETH for YB_tETH and vice versa",
			"lineHeight": 1.25,
			"baseline": 44
		},
		{
			"id": "mcaENwp9ry5N66dslcu2i",
			"type": "rectangle",
			"x": 0,
			"y": -160,
			"width": 1000,
			"height": 320,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 784872506,
			"version": 32,
			"versionNonce": 2139934054,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1727690504446,
			"link": null,
			"locked": false
		},
		{
			"id": "RwpTObWy",
			"type": "text",
			"x": 380,
			"y": -140,
			"width": 213.0998077392578,
			"height": 25,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1973611706,
			"version": 6,
			"versionNonce": 1905704742,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1727690504446,
			"link": null,
			"locked": false,
			"text": "Questions / comments",
			"rawText": "Questions / comments",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "top",
			"baseline": 17,
			"containerId": null,
			"originalText": "Questions / comments",
			"lineHeight": 1.25
		},
		{
			"id": "AZBIG8gE",
			"type": "text",
			"x": 40,
			"y": -80,
			"width": 189.83984375,
			"height": 25,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1520307130,
			"version": 40,
			"versionNonce": 1679218426,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1727690504446,
			"link": null,
			"locked": false,
			"text": "example question 1 ",
			"rawText": "example question 1 ",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 17,
			"containerId": null,
			"originalText": "example question 1 ",
			"lineHeight": 1.25
		},
		{
			"id": "ZiZGNt8SpTuQZenwKVTAh",
			"type": "arrow",
			"x": 180,
			"y": -40,
			"width": 60,
			"height": 460,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"seed": 2098444646,
			"version": 128,
			"versionNonce": 782347686,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1727690504446,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-60,
					460
				]
			],
			"lastCommittedPoint": [
				-60,
				460
			],
			"startBinding": null,
			"endBinding": null,
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "YMbtB8VCeXMU_PCPEA2yO",
			"type": "arrow",
			"x": 980,
			"y": 1120,
			"width": 300,
			"height": 60,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"seed": 1963192742,
			"version": 37,
			"versionNonce": 1975779878,
			"isDeleted": true,
			"boundElements": [
				{
					"type": "text",
					"id": "kk8pZ0e7"
				}
			],
			"updated": 1727690504446,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-300,
					-60
				]
			],
			"lastCommittedPoint": [
				-300,
				-60
			],
			"startBinding": null,
			"endBinding": {
				"elementId": "OCuA2lA-gUCqjeQMIEepF",
				"focus": -0.6202531645569619,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "kk8pZ0e7",
			"type": "text",
			"x": 811.0200119018555,
			"y": 1077.5,
			"width": 37.95997619628906,
			"height": 25,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1791351206,
			"version": 21,
			"versionNonce": 974199610,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1727690504446,
			"link": null,
			"locked": false,
			"text": "??? ",
			"rawText": "??? ",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 17,
			"containerId": "YMbtB8VCeXMU_PCPEA2yO",
			"originalText": "??? ",
			"lineHeight": 1.25
		},
		{
			"id": "vroLfHXi",
			"type": "text",
			"x": 495,
			"y": -12.5,
			"width": 10,
			"height": 25,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1623558950,
			"version": 5,
			"versionNonce": 645768186,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1727690504446,
			"link": null,
			"locked": false,
			"text": "",
			"rawText": "",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 17,
			"containerId": "mcaENwp9ry5N66dslcu2i",
			"originalText": "",
			"lineHeight": 1.25
		},
		{
			"id": "5OK8Jaoh",
			"type": "text",
			"x": 181.3961181640625,
			"y": -78.16661071777344,
			"width": 10,
			"height": 25,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 774570490,
			"version": 5,
			"versionNonce": 1150955686,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1727690504446,
			"link": null,
			"locked": false,
			"text": "",
			"rawText": "",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 17,
			"containerId": null,
			"originalText": "",
			"lineHeight": 1.25
		},
		{
			"id": "kauNLwqK",
			"type": "text",
			"x": 521.5499038696289,
			"y": -100,
			"width": 10,
			"height": 25,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1970863654,
			"version": 65,
			"versionNonce": 232461498,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1727690504446,
			"link": null,
			"locked": false,
			"text": "",
			"rawText": "",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "top",
			"baseline": 17,
			"containerId": null,
			"originalText": "",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 33,
			"versionNonce": 546909158,
			"isDeleted": true,
			"id": "2XgLLM820JMhO7tVxAK2x",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -60,
			"y": -320,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1000,
			"height": 320,
			"seed": 200932858,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1727690504446,
			"link": null,
			"locked": false
		},
		{
			"id": "ARlUMPsn",
			"type": "text",
			"x": 386.8462142944336,
			"y": -104.16661071777344,
			"width": 213.0998077392578,
			"height": 25,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1838677242,
			"version": 3,
			"versionNonce": 835480954,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1727690504446,
			"link": null,
			"locked": false,
			"text": "Questions / comments",
			"rawText": "Questions / comments",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "top",
			"baseline": 17,
			"containerId": null,
			"originalText": "Questions / comments",
			"lineHeight": 1.25
		},
		{
			"id": "paYbCyNH",
			"type": "text",
			"x": 82.3961181640625,
			"y": -36.16661071777344,
			"width": 10,
			"height": 25,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1269912230,
			"version": 3,
			"versionNonce": 664055354,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1727690504446,
			"link": null,
			"locked": false,
			"text": "",
			"rawText": "",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "top",
			"baseline": 17,
			"containerId": null,
			"originalText": "",
			"lineHeight": 1.25
		},
		{
			"id": "McuGPCiu",
			"type": "text",
			"x": 84.3961181640625,
			"y": -50.16661071777344,
			"width": 10,
			"height": 25,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 429530746,
			"version": 5,
			"versionNonce": 1275062886,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1727690504446,
			"link": null,
			"locked": false,
			"text": "",
			"rawText": "",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "top",
			"baseline": 17,
			"containerId": null,
			"originalText": "",
			"lineHeight": 1.25
		}
	],
	"appState": {
		"theme": "light",
		"viewBackgroundColor": "#ffffff",
		"currentItemStrokeColor": "#1e1e1e",
		"currentItemBackgroundColor": "transparent",
		"currentItemFillStyle": "solid",
		"currentItemStrokeWidth": 2,
		"currentItemStrokeStyle": "solid",
		"currentItemRoughness": 1,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 1,
		"currentItemFontSize": 20,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": 103.3955078125,
		"scrollY": -265.83335876464844,
		"zoom": {
			"value": 1
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