---
layout: single
author_profile: true
title: "Four-in-a-row demo"
excerpt: "Planning task (ongoing project)."
header:
 teaser: assets/images/4inarow.png
---

We are using a game called Four-in-a-row to identify the developmental trajectories of cognitive components that underlie complex planning. This is a collaboration with the [Hartley lab](https://www.hartleylab.org/). The original task and computational models were developed by [van Opheusden et al.](https://basvanopheusden.github.io/)

Check out our [preprint](https://psyarxiv.com/7fqsr).

Click on a tile to place a stone. You play against the computer. Whoever gets four in a row first wins.

<link href = "/assets/4inarow/stylesheet.css" rel="stylesheet">
<link href= " https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">
<div class="modal fade blackshadow" id="feedback-modal" data-backdrop="static" role="dialog" aria-hidden="true">
	<div class="modal-dialog modal-sm">
		<div class="modal-content">
			<div class="modal-body">
				<h2 class="modal-title">Good game!</h2>
				<div class='row'>
					<div class='col-xs-10 col-xs-offset-1 text-center' id='scorebox'>
						<div id='p0-score' class='col-xs-6 text-center'>
							<h4>You:</h4>
							<h2>0</h2>
						</div>
						<div id='p1-score' class='col-xs-6 text-center'>
							<h4>Computer:</h4>
							<h2>0</h2>
						</div>
					</div>
				</div>
			<button class="btn btn-large btn-warning" id="next-trial">Play Again</button>
			</div>
		</div>
	</div>
</div>

<div class='container-fluid text-center'>
	<div class='row'>
		<div class="headertext">
			Your turn
		</div>
	</div>
	<div class="row">
		<div class="container-fluid col-xs-8 canvas-container">
			<div class="canvas"></div>
		</div>
	</div>
</div>

<script src="/assets/4inarow/underscore-min.js"></script>
<script src="/assets/4inarow/util.js"></script>
<script src="/assets/4inarow/game.js"></script>
<script src="/assets/4inarow/AI.js"></script>
<script src="/assets/4inarow/makemove.js"></script>

<script>
	var blocks, player;
	M=9;
	N=4;
	K=4;
	current_block = 0;

	window.onload = () => {
		player = new Player();
		board = new Board();
		board.create_tiles()
		blocks = [new Condition_AI(60)];
		blocks[current_block].run();
	};
</script>
