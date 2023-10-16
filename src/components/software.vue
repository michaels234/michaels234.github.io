<script>
	import softwareCard from './softwareCard.vue'

	export default {
		components: {
			softwareCard,
		},
		mounted () {
			//this.checkImages()
		},
		methods: {
			checkImages () {
				let cardsEl = this.$refs.cards
				let images = cardsEl.querySelectorAll("img")
				let imagesLoadCount = 0
				images.forEach((img) => {
					if (img.complete) {
						imagesLoadCount++;
						if (imagesLoadCount === images.length) {
							this.setGridRowHeight(cardsEl);
						}
					} else {
						img.addEventListener("load", () => {
							imagesLoadCount++;
							if (imagesLoadCount === images.length) {
								this.setGridRowHeight(cardsEl);
							}
						});
					}
				});
			},
			setGridRowHeight (cardsEl) {
				let maxHeight = 0
				cardsEl.childNodes.forEach((child) => {
					if (child.nodeType !== Node.ELEMENT_NODE) {
						return;
					} else {
						let height = child.offsetHeight
						if (height > maxHeight) {
							maxHeight = height
						}
					}
				})
				if (maxHeight) {
					console.log(maxHeight)
					this.$refs.cards.style.gridAutoRows = "minmax(" + maxHeight + "px, 9999px)"
				}
			}
		}
	}
</script>

<template>
	<div class="scrolling cards" ref="cards">
		<softwareCard
			link="https://michaelsime.one/"
			git="https://github.com/michaels234/michaels234.github.io/"
			image="src/assets/michaelsimeone.png"
			title="michaelsime.one Home Page"
			:message="`The website you're on right now.
CSS, HTML, Node.js, JavaScript, Vite, Vue.js`"
		/>
		<softwareCard
			link="https://michaelsime.one/movieRecommendation/"
			git="https://github.com/michaels234/movieRecommendation/"
			image="src/assets/movierecs.png"
			title="Movie Recommendations"
			:message="`A web app that uses machine learning to recommend movies similar to a movie input by the user.
AWS API Gateway, AWS DynamoDB, AWS Lambda, CSS, GitHub Pages, HTML, JavaScript, NLP, Node.js, NumPy, Pandas, Python, React, scikit-learn`"
		/>
		<softwareCard
			link="https://play.unity.com/mg/other/webgl-builds-238852/"
			git="https://github.com/michaels234/spaceGame/"
			image="src/assets/spacegame.png"
			title="Space Game"
			:message="`An open world 3D space game.
Blender, C#, Unity`"
		/>
		<softwareCard
			link="https://eventhorizonvip.pythonanywhere.com/"
			git="https://github.com/TecKno3/EventHorizon/"
			image="src/assets/eventhorizon.png"
			title="Event Horizon"
			:message="`Event hosting web & mobile app and business strategy.
AWS, CSS, Django REST, Google Cloud, HTML, JavaScript, Node.js, PostgreSQL, Python, SQLite, Vue.js`"
		/>
		<softwareCard
			link=""
			git="https://github.com/michaels234/Japanese/"
			image="src/assets/noimageyet.png"
			title="Japanese - English Study Web App"
			:message="`An app for English speakers to study Japanese.
CSS, FastAPI, HTML, JavaScript, Node.js, Python, SQLite, Vite, Vue.js`"
		/>
	</div>
</template>

<style scoped>
	.cards {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		grid-auto-rows: max-content;
		grid-gap: 3%;
		height: 100%;
		position: relative;
	}
	@media (max-width: 800px) {
		.cards {
			grid-template-columns: repeat(1, minmax(0, 1fr));
		}
	}
</style>
