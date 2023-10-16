<script>

export default {
	data () {
		return {
			resumeimage: new URL('../assets/resume.png', import.meta.url).href,
		}
	},
	methods: {
		download () {
			window.location.href='@/assets/Resume_Michael_Simeone_Site_Japan.pdf'
		}
	}
}
</script>

<template>
	<div class="full">
		<a href="@/assets/Resume_Michael_Simeone_Site_Japan.pdf" class="click" download>
			<button>
				Click to Download
			</button>
		</a>
		<a href="@/assets/Resume_Michael_Simeone_Site_Japan.pdf" class="image scrolling" download>
			<img :src="resumeimage" />
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
