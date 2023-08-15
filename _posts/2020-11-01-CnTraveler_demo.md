---
layout: single
author_profile: true
title: "Canadian Traveler Game demo"
excerpt: "Information sampling in a navigation task (ongoing project)."
header:
 teaser: assets/images/Sheep.png
---

Navigate the sheep to the goal across the bridges in as few actions as possible.
The status of a bridge can be  “open” (green), “closed” (red), or “unknown” (grey).
All bridges start as “unknown” at the beginning of a new puzzle.

In stage 1, clicking on a bridge reveals its status and you can sample the status of up to ten bridges anywhere in the puzzle.
You can stop sampling by clicking on the “stop checking” button.
In stage 2, you can move the sheep by clicking on a bridge adjacent to the sheep.
The goal of the task is to get the sheep to the goal in as few a samples and sheep moves as possible, as each incurs a cost.

<link rel="stylesheet" href="/Voyager_build/TemplateData/style.css" type="text/css">
<script src="/Voyager_build/Build/Voyager_build.loader.js"></script>
<canvas id="unity-canvas" width=960 height=600 tabindex="-1" style="width: 960px; height: 600px; background: #231F20"></canvas>
<textarea rows="5" cols="80" name="Log" id="logField" required style="display: none;"></textarea>
<script>
	var RuleVariant = "TwoStage";
	var skipTutorial = true;
	createUnityInstance(document.querySelector("#unity-canvas"), {
		dataUrl: "/Voyager_build/Build/Voyager_build.data.unityweb",
		frameworkUrl: "/Voyager_build/Build/Voyager_build.framework.js.unityweb",
		codeUrl: "/Voyager_build/Build/Voyager_build.wasm.unityweb",
		streamingAssetsUrl: "StreamingAssets",
		companyName: "DefaultCompany",
		productName: "Voyager",
		productVersion: "0.1",
		// matchWebGLToCanvasSize: false, // Uncomment this to separately control WebGL canvas render size and DOM element size.
		// devicePixelRatio: 1, // Uncomment this to override low DPI rendering on high DPI displays.
	});
</script>