<script lang="ts">
	import Icon from '@iconify/svelte';
	export let rotate: 'left' | 'right' | 'up' | 'down' = 'down';
</script>

<div class="down-arrow {rotate}">
	<Icon icon="material-symbols:arrow-back-ios-new-rounded" />
</div>

<style>
	.down-arrow {
		rotate: 270deg;
		margin-bottom: 10vh;
	}

	.left {
		rotate: 0deg;
	}
	.right {
		rotate: 180deg;
	}
	.up {
		rotate: 90deg;
	}
	.down {
		rotate: 270deg;
	}
</style>
