<script>
	import mainDisplay from './components/main-display.vue'

	export default {
		components: {
			mainDisplay,
		}
	}
</script>

<template>
	<html>
		<body>
			<div class="app">
				<div class="title">
					<div>MICHAEL</div>
					<div>SIMEONE</div>
				</div>
				<div class="main">
					<mainDisplay/>
				</div>
			</div>
		</body>
	</html>
</template>

<style>
	body {
		margin: 0; /*important for forcing to it to the very edge*/
		font-size: 1vw;
	}
	.app {
		height: 100vh; /*important for forcing to it to fit within body*/
		background: linear-gradient(160deg, #003f7a, 80%, #3c9df8);
		font-family: -apple-system, BlinkMacSystemFont, sans-serif;
		color: #a0a0a0;
		font-weight: 500;
		display: flex;
		flex-direction: column;
		justify-content: flex-start;
		align-items: center;
	}
	.title {
		text-align: center;
		font-size: 9em;
		font-weight: bold;
		line-height: 0.8;
		height: fit-content;
		padding: 3vh;
	}
	.main {
		display: flex;
		flex-direction: column;
		width: 82%;
		flex: 1 0 0;
	}
	button, .button {
		font: inherit;
		font-size: 1em;
		color: inherit;
		text-decoration: none;
		margin-bottom: 1%;
		background-color: #003f7a;
		border: none;
		box-shadow: inset 0 0 7px 1px #002c55;
		box-sizing: border-box;
		border-radius: 10px;
		padding: 1% 3% 1% 3%;
		width: fit-content;
		white-space: pre;
	}
	button:active {
		box-shadow: inset 0 0 10px 5px #002141;
		color: #929292;
		background-color: #003668;
	}
	button:hover {
		cursor: pointer;
	}
	.button-inactive {
		font: inherit;
		font-size: 1em;
		color: inherit;
		text-decoration: none;
		margin-bottom: 1%;
		background-color: #335474;
		border: none;
		box-shadow: inset 0 0 7px 1px #002c55;
		box-sizing: border-box;
		border-radius: 10px;
		padding: 1% 3% 1% 3%;
		width: fit-content;
		white-space: pre;
	}
	.button-inactive:active {
		box-shadow: inset 0 0 7px 1px #002c55;
		color: #a0a0a0;
		background-color: #335474;
	}
	.button-inactive:hover {
		cursor: default;
	}
	a {
		font: inherit;
		font-size: 3em;
		color: inherit;
		text-decoration: none;
	}
	.scrolling {
		overflow-y: auto !important;
	}
	.scrolling::-webkit-scrollbar-track {
		-webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0.3);
		border-radius: 10px;
		background: linear-gradient(160deg, #003f7a, 80%, #3c9df8);
	}
	.scrolling::-webkit-scrollbar {
		width: 12px;
		background: linear-gradient(160deg, #003f7a, 80%, #1775ce);
		-webkit-box-shadow: inset 0 0 1px #3c9df8;
	}
	.scrolling::-webkit-scrollbar-thumb {
		border-radius: 10px;
		-webkit-box-shadow: inset 0 0 6px rgba(0,0,0,.9);
		background: linear-gradient(160deg, #003f7a, 80%, #1775ce);
	}
	@media (max-width: 600px) {
		.main {
			width: 95%;
		}
	}
	@media (min-width: 1000px) {
		body {
			font-size: 10px;
		}
		.main {
			width: 820px;
		}
	}
</style>
