<template>
	<div class="v2dp-toggle-sub-mode">
		<button class="v2dp-toggle-sub-mode-button"
			@click="$emit('multiple-toggle')"
		>
			<img class="v2dp-controls-icon-mode-toggle"
				:src="icon"
				alt="mode-toggle" 
			>
		</button>
	</div>
</template>

<script>
export default {
	name: 'VMultipleToggle',
	props: {
		icon: {
			type: String,
			default: ''
		}
	}
}
</script>

<style lang="scss">
	.v2dp-toggle-sub-mode {
		width: 100%;
		display: flex;
		justify-content: center;
		position: relative;
		bottom: -15px;
	}

	.v2dp-controls-icon-mode-toggle {
		width: var(--size-circle-toggle);
		height: var(--size-circle-toggle);
		transform: rotate(180deg);
		transition: filter .2s;

		&:hover {
			filter: brightness(.5);
		}
	}
</style>