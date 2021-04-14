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

<link rel="stylesheet" href="https://ili-ma.github.io/Voyager_build/TemplateData/style.css" type="text/css">
<script src="https://ili-ma.github.io/Voyager_build/TemplateData/UnityProgress.js"></script>
<script src="https://ili-ma.github.io/Voyager_build/Build/UnityLoader.js"></script>
<script>
	var RuleVariant = "TwoStage";
	var skipTutorial = true;
	var unityInstance = UnityLoader.instantiate("unityContainer", "https://ili-ma.github.io/Voyager_build/Build/Voyager_build.json", {onProgress: UnityProgress});
</script>
<div id="webgl-content">
	<div id="unityContainer" style="width: 800px; height: 500px"></div>
	<div class="footer">
		<p id="progress"></p>
	</div>
</div>
<textarea rows="5" cols="80" name="Log" id="logField" required style="display: none;"></textarea>
