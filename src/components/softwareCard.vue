<script>
	import links from './links.vue'

	export default {
		components: {
			links,
		},
		props: {
			link: String,
			git: String,
			image: String,
			title: String,
			message: String,
		},
		data() {
			return {
				showLinks: false,
			}
		},
	}
</script>

<template>
	<div>
		<button class="card" v-if="(link || git) && !showLinks" @click="showLinks=true">
			<img :src="image" />
			<div class="title-text">{{ title }}</div>
			<div>{{ message }}</div>
		</button>
		<button class="card button-inactive" v-else-if="!link && !git">
			<div class="no-link">No Link</div>
			<img :src="image" />
			<div class="title-text">{{ title }}</div>
			<div>{{ message }}</div>
		</button>
		<div class="button card" v-else-if="showLinks">
			<img :src="image" />
			<div class="title-text">{{ title }}</div>
			<div class="links">
				<button class="back" @click="showLinks=false">
					⇦ Description
				</button>
				<a :href="link" target="_blank" v-if="link">
					<button class="link">
						Open Web App
					</button>
				</a>
				<a :href="git" target="_blank" v-if="git">
					<button class="link">
						Open Git
					</button>
				</a>
			</div>
		</div>
	</div>
</template>

<style scoped>
	.card {
		position: relative;
		border-radius: 10px;
		font-size: 2.5em;
		display: flex;
		flex-direction: column;
		justify-content: flex-start;
		align-items: center;
		width: 100%;
		height: 100%;
		white-space: pre-wrap;
		padding: 3%;
	}
	img {
		width: 50%;
		height: auto;
		border-radius: 10px;
		margin-bottom: 3%;
	}
	.title-text {
		font-weight: bold;
		font-size: 1.1em;
		padding-bottom: 2%;
		text-align: center;
	}
	.no-link {
		position: absolute;
		right: 2%;
		font-size: 0.8em;
	}
	.links {
		position: relative;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 100%;
		width: 100%;
	}
	a {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		margin-top: 3%;
		margin-bottom: 3%;
		width: 100%;
	}
	.link {
		font-size: 0.5em;
		padding: 3%;
	}
	.back {
		font-size: 1.5em;
		padding: 3%;
		margin-top: 3%;
		margin-bottom: 3%;
	}
	button {
		width: 80%;
	}
</style>
