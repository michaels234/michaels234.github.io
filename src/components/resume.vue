<script>
export default {
	methods: {
		download () {
			window.location.href='src/assets/Resume_Michael_Simeone_Site_Japan.pdf'
		}
	}
}
</script>

<template>
	<div class="full">
		<a href="src/assets/Resume_Michael_Simeone_Site_Japan.pdf" class="click" download>
			<button>
				Click to Download
			</button>
		</a>
		<a href="src/assets/Resume_Michael_Simeone_Site_Japan.pdf" class="image scrolling" download>
			<img src="src/assets/resume.png" />
		</a>
	</div>
</template>

<style scoped>
	.full {
		width: 100%;
		height: 100%;
		overflow-y: hidden;
		display: flex;
		flex-direction: column;
		justify-content: flex-start;
		align-items: center;
	}
	.click {
		margin-bottom: 2%;
		width: fit-content;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
	img {
		width: 90%;
		height: auto;
		background-color: white;
		padding: 5%;
	}
	.image {
		width: 100%;
		height: 100%;
	}
</style>
