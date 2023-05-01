<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">
	<title>Campus Square Food Roulette</title>
	<link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
	<div class="roulette-container">
		<h1>Campus Square Food Roulette</h1>
		<div id="roulette" class="roulette">
			<div class="label"><img src="images/kfc.png"></div>
			<div class="label"><img src="images/mcd.png"></div>
			<div class="label"><img src="images/wimpy.png"></div>
			<div class="label"><img src="images/rocco.png"></div>
			<div class="label"><img src="images/chicken.png"></div>
		</div>
		<button id="spin" class="spin-btn">SPIN</button>
	</div>
	<audio id="spin-sound" src="sounds/spin.mp3"></audio>
	<audio id="win-sound" src="sounds/win.mp3"></audio>
	<script src="script.js"></script>
</body>
</html>
<style>
	body {
		background-image: url("https://www.foodiesfeed.com/wp-content/uploads/2019/05/top-view-for-classic-burgers.jpg");
		background-size: cover;
		background-repeat: no-repeat;
		background-position: center;
	}

	.roulette-container {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin-top: 50px;
		color: white;
	}

	h1 {
		font-size: 36px;
		margin-bottom: 50px;
	}

	.roulette {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		align-items: center;
		width: 500px;
		height: 500px;
		border-radius: 50%;
		background-color: white;
		position: relative;
		overflow: hidden;
		box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
	}

	.roulette .label {
		display: flex;
		justify-content: center;
		align-items: center;
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		font-size: 24px;
		font-weight: bold;
		color: white;
		transform-origin: center center;
		transition: transform 3s cubic-bezier(0.25, 0.1, 0.25, 1);
	}

	.roulette .label img {
		max-width: 80%;
		max-height: 80%;
	}

	.spin-btn {
		padding: 10px 20px;
		font-size: 24px;
		background-color: #2196F3;
		color: white;
		border: none;
		border-radius: 5px;
		cursor: pointer;
		margin-top: 50px;
		transition: background-color 0.3s ease-in-out;
	}

	.spin-btn:hover {
		background-color: #0D47A1;
	}
</style>
// Play win sound after 3 seconds
const winSound = document.querySelector('#win-sound');
setTimeout(() => {
  winSound.play();
}, spinTime);

// Update UI after 3.5 seconds
setTimeout(() => {
  spinning = false;
  spinBtn.disabled = false;
  alert(`You got ${labels[stopIndex].textContent}!`);
}, spinTime + 500);
