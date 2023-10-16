<script>
	import tab from './tab.vue'
	import about from './about.vue'
	import resume from './resume.vue'
	import software from './software.vue'

	export default {
		components: {
			tab,
			about,
			software,
			resume,
		},
		data() {
			return {
				selected: 'Software'
			}
		},
		methods: {
			select (name) {
				this.selected = name
			},
			isSelected(name) {
				return this.selected === name
			}
		}
	}
</script>

<template>
	<div class="tabs">
		<!--<tab :name="'About'" :selected="selected" @select="name => select(name)" />-->
		<tab :name="'Software'" :selected="selected" @select="name => select(name)" />
		<tab :name="'Resume'" :selected="selected" @select="name => select(name)" />
		<!--<tab :name="'Music'" :selected="selected" @select="name => select(name)" />-->
	</div>
	<div class="displayed">
		<!--<about v-if="isSelec`ted('About')" />-->
		<software v-if="isSelected('Software')"/>
		<resume v-else-if="isSelected('Resume')" />
	</div>
</template>

<style scoped>
	.tabs {
		width: 100%;
		display: flex;
		margin-bottom: 20px;
	}
	.displayed {
		position: relative;
		overflow-y: hidden;
		flex: 1 0 0;
	}
	@media (max-width: 600px) {
		.tabs {
			font-size: 6px;
		}
	}
</style>
