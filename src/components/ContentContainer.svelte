<script lang="ts">
	import NextEvent from './NextEvent.svelte';

	export let backgroundColor: string = 'white';
</script>

<div class="outer">
	<div class="inner">
		<NextEvent />
	</div>
</div>

<style>
	.outer {
		/* Set up SCSS to make this dynamic */
		background: rgb(14, 223, 243);
		background: linear-gradient(180deg, rgba(14, 223, 243, 1) 0%, rgba(22, 156, 141, 1) 100%);
		margin: 1rem;
		border-radius: 1.5rem;
		display: flex;
		align-items: center;
	}

	.inner {
		background-color: white;
		width: 98%;
		margin: 5px;
		border-radius: 1.2rem;
	}
</style>
