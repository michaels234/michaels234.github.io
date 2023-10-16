<script>
	export default {
		props: {
			name: {},
			selected: {}
		},
		methods: {
			isSelected() {
				return this.selected === this.name
			}
		}
	}
</script>

<template>
	<div :class="isSelected() ? 'selected' : 'tab'" @click="$emit('select', name)">
		{{ name }}
	</div>
</template>

<style scoped>
	.tab, .selected {
		height: 100%;
		font-size: 3em;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		font-weight: bold;
		flex: 1 0 0;
		border-bottom: 2px solid #777777;
		box-sizing: border-box;
		cursor: pointer;
	}

	.selected {
		color: #00ccb4;
		border-bottom: 2px solid #00ccb4;
		box-sizing: border-box;
      	text-shadow: 0 0 5px #00ffe1ad;
	}
</style>
