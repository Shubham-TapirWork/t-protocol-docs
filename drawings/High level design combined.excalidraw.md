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

Fixed yield module ^sA7oXaII

Deposit tETH (receive 1 PT_tETH + 1YT_tETH) ^m1X60X9F

AMM for 
PT_tETH / tETH  ^neT5egBB

Swap PT_tETH for tETH and vice versa ^vnpkMnmw

NOTE: 
If user wants DP_tETH, 
they will buy it straight from the pool
IF
user wants YB_tETH, 
they will mint both and sell DP_tETH into the pool
 

  ^qxNuTBh2

NOTE: 
If user wants PT_tETH, 
they will buy it straight from the pool
IF
user wants YT_tETH, 
they will mint both and sell PT_tETH into the pool
 

  ^YbCFL1G2

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
			"version": 218,
			"versionNonce": 1113699258,
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
			"updated": 1727691974854,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 186,
			"versionNonce": 1418722534,
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
			"updated": 1727691974854,
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
			"version": 238,
			"versionNonce": 2049387642,
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
			"updated": 1727691974854,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 99,
			"versionNonce": 9138214,
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
			"updated": 1727691974854,
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
			"version": 186,
			"versionNonce": 876580154,
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
			"updated": 1727691974854,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 127,
			"versionNonce": 1530297190,
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
			"updated": 1727691974854,
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
			"version": 479,
			"versionNonce": 1980618234,
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
			"updated": 1727691974854,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 468,
			"versionNonce": 450764454,
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
			"updated": 1727691974854,
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
			"version": 320,
			"versionNonce": 546637498,
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
			"updated": 1727691974854,
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
			"version": 53,
			"versionNonce": 607082982,
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
			"updated": 1727691974854,
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
			"version": 391,
			"versionNonce": 2088247162,
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
			"updated": 1727691974854,
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
			"version": 53,
			"versionNonce": 1043803430,
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
			"updated": 1727691974854,
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
			"version": 272,
			"versionNonce": 1174020154,
			"isDeleted": false,
			"id": "CCAsimPEqxHX4MHRXGzjL",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 648.5751454829822,
			"y": 600.3488601203175,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 43.35327802345728,
			"height": 76.25588287893686,
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
			"updated": 1727691974854,
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
					-43.35327802345728,
					76.25588287893686
				]
			]
		},
		{
			"type": "text",
			"version": 39,
			"versionNonce": 1180866662,
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
			"updated": 1727691974854,
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
			"version": 250,
			"versionNonce": 956172538,
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
			"updated": 1727691974854,
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
			"version": 38,
			"versionNonce": 1686018982,
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
			"updated": 1727691974854,
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
			"version": 569,
			"versionNonce": 486988218,
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
			"updated": 1727691974854,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 563,
			"versionNonce": 1052260070,
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
			"updated": 1727691974854,
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
			"version": 558,
			"versionNonce": 1362596474,
			"isDeleted": false,
			"id": "osWU5rRy9qNaplwaj9c6j",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 821.0274266475419,
			"y": 596.9760416604578,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 76.9849282500436,
			"height": 87.03712293836804,
			"seed": 924845124,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1727691974854,
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
					76.9849282500436,
					87.03712293836804
				]
			]
		},
		{
			"type": "arrow",
			"version": 496,
			"versionNonce": 765225510,
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
			"updated": 1727691974854,
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
			"version": 320,
			"versionNonce": 1481847610,
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
			"updated": 1727691974854,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 273,
			"versionNonce": 1880634726,
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
			"updated": 1727691974854,
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
			"version": 525,
			"versionNonce": 1690090490,
			"isDeleted": false,
			"id": "aI9ze98tlK67P0Ek_5NO2",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 99.03507834567478,
			"y": 678.7927761099916,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 240.77520758459582,
			"height": 302.46037959024693,
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
			"updated": 1727691974854,
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
					240.77520758459582,
					302.46037959024693
				]
			]
		},
		{
			"type": "text",
			"version": 78,
			"versionNonce": 1601738918,
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
			"updated": 1727691974855,
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
			"version": 394,
			"versionNonce": 1685531834,
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
			"updated": 1727691974855,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 384,
			"versionNonce": 449410982,
			"isDeleted": false,
			"id": "rI5QapIB",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 937.4800491333008,
			"y": 1025,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 165.03990173339844,
			"height": 50,
			"seed": 55224954,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727692053967,
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
			"version": 1057,
			"versionNonce": 2014473126,
			"isDeleted": false,
			"id": "qvSMzYA-1blZ_3hkkrk-z",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 81.09379427954553,
			"y": 680.9436679430306,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 719.0297937375872,
			"height": 576.9944592600893,
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
			"updated": 1727692065414,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			},
			"startBinding": {
				"elementId": "7F4kaJTp_7WpER2FSfqmg",
				"focus": 0.3518378504505029,
				"gap": 20.947607196291642
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
					200.02979373758689,
					576.9944592600893
				],
				[
					719.0297937375872,
					516.9817745787022
				]
			]
		},
		{
			"type": "text",
			"version": 129,
			"versionNonce": 875587686,
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
			"width": 347.23974609375,
			"height": 25,
			"seed": 1769337018,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727692063853,
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
			"version": 45,
			"versionNonce": 1745536570,
			"isDeleted": false,
			"id": "mcaENwp9ry5N66dslcu2i",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 0,
			"y": -160,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1000,
			"height": 320,
			"seed": 784872506,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1727691974855,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 19,
			"versionNonce": 127357542,
			"isDeleted": false,
			"id": "RwpTObWy",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 380,
			"y": -140,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 213.0998077392578,
			"height": 25,
			"seed": 1973611706,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727691974855,
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
			"version": 53,
			"versionNonce": 1577709306,
			"isDeleted": false,
			"id": "AZBIG8gE",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 40,
			"y": -80,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 189.83984375,
			"height": 25,
			"seed": 1520307130,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727691974855,
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
			"version": 141,
			"versionNonce": 1393300902,
			"isDeleted": false,
			"id": "ZiZGNt8SpTuQZenwKVTAh",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 180,
			"y": -40,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 60,
			"height": 460,
			"seed": 2098444646,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1727691974855,
			"link": null,
			"locked": false,
			"startBinding": null,
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
					-60,
					460
				]
			]
		},
		{
			"type": "rectangle",
			"version": 356,
			"versionNonce": 1134952378,
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
			"updated": 1727691974855,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 309,
			"versionNonce": 830894310,
			"isDeleted": false,
			"id": "sA7oXaII",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 412.24292699822456,
			"y": 1386.4542240902786,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 155.537109375,
			"height": 25,
			"seed": 1931556326,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727691974855,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 5,
			"text": "Fixed yield module",
			"rawText": "Fixed yield module",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": "tGq6v-UEsBS5_yOaI2T56",
			"originalText": "Fixed yield module",
			"lineHeight": 1.25,
			"baseline": 19
		},
		{
			"type": "arrow",
			"version": 740,
			"versionNonce": 1694627962,
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
			"updated": 1727691974855,
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
			"version": 93,
			"versionNonce": 1586717734,
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
			"width": 190.119873046875,
			"height": 50,
			"seed": 1871541350,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727691974855,
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
			"version": 426,
			"versionNonce": 299948346,
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
			"updated": 1727691974855,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			}
		},
		{
			"type": "text",
			"version": 412,
			"versionNonce": 471854950,
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
			"updated": 1727691974855,
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
			"version": 1257,
			"versionNonce": 698720762,
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
			"updated": 1727691974855,
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
			"version": 129,
			"versionNonce": 1719210662,
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
			"width": 314.07977294921875,
			"height": 25,
			"seed": 1861554534,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1727691974855,
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
			"id": "qxNuTBh2",
			"type": "text",
			"x": 820,
			"y": 1100,
			"width": 360.01568603515625,
			"height": 159.54156660561478,
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
			"seed": 1646869158,
			"version": 312,
			"versionNonce": 659772090,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "qvSMzYA-1blZ_3hkkrk-z",
					"type": "arrow"
				}
			],
			"updated": 1727691974855,
			"link": null,
			"locked": false,
			"text": "NOTE: \nIf user wants DP_tETH, \nthey will buy it straight from the pool\nIF\nuser wants YB_tETH, \nthey will mint both and sell DP_tETH into the pool\n \n\n ",
			"rawText": "NOTE: \nIf user wants DP_tETH, \nthey will buy it straight from the pool\nIF\nuser wants YB_tETH, \nthey will mint both and sell DP_tETH into the pool\n \n\n ",
			"fontSize": 14.181472587165757,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 154,
			"containerId": null,
			"originalText": "NOTE: \nIf user wants DP_tETH, \nthey will buy it straight from the pool\nIF\nuser wants YB_tETH, \nthey will mint both and sell DP_tETH into the pool\n \n\n ",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 331,
			"versionNonce": 676056550,
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
			"updated": 1727691974855,
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
			"id": "1ahwZeJhHre__tt8_WKf7",
			"type": "rectangle",
			"x": 260,
			"y": 960,
			"width": 999.9999999999999,
			"height": 320,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 975592934,
			"version": 35,
			"versionNonce": 1836575098,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1727692057780,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 49,
			"versionNonce": 311782458,
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
			"boundElements": [],
			"updated": 1727691974855,
			"link": null,
			"locked": false
		},
		{
			"id": "jEBn5Sc9",
			"type": "text",
			"x": 755,
			"y": 1107.5,
			"width": 10,
			"height": 25,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 25203046,
			"version": 2,
			"versionNonce": 1483778618,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1727692057783,
			"link": null,
			"locked": false,
			"text": "",
			"rawText": "",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 17,
			"containerId": "1ahwZeJhHre__tt8_WKf7",
			"originalText": "",
			"lineHeight": 1.25
		},
		{
			"id": "YNg5K4I6",
			"type": "text",
			"x": 755,
			"y": 1107.5,
			"width": 10,
			"height": 25,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1808569702,
			"version": 5,
			"versionNonce": 1856315686,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1727691974855,
			"link": null,
			"locked": false,
			"text": "",
			"rawText": "",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 17,
			"containerId": "1ahwZeJhHre__tt8_WKf7",
			"originalText": "",
			"lineHeight": 1.25
		},
		{
			"id": "cEG4kiod",
			"type": "text",
			"x": 651.1742054332386,
			"y": -51.21201948686087,
			"width": 80.85992431640625,
			"height": 25,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1513056230,
			"version": 27,
			"versionNonce": 485624934,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1727691974855,
			"link": null,
			"locked": false,
			"text": "Comment",
			"rawText": "Comment",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 17,
			"containerId": null,
			"originalText": "Comment",
			"lineHeight": 1.25
		},
		{
			"id": "UDJvpRNv",
			"type": "text",
			"x": 612.3863636363636,
			"y": -63.333268599076746,
			"width": 95.69992065429688,
			"height": 50,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1612924198,
			"version": 19,
			"versionNonce": 7521894,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1727691981997,
			"link": null,
			"locked": false,
			"text": "Comment: \n? use ",
			"rawText": "Comment: \n? use ",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 42,
			"containerId": null,
			"originalText": "Comment: \n? use ",
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
		"currentItemStrokeStyle": "dashed",
		"currentItemRoughness": 1,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 1,
		"currentItemFontSize": 20,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": 109.73488547585225,
		"scrollY": 104.54548228870732,
		"zoom": {
			"value": 0.55
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