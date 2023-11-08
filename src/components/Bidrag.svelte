<script lang="ts">
	export let title: string = 'Bidragstitel';
	import PdfViewer from 'svelte-pdf';
</script>

<div class="page">
	<div class="container">
		<h1>{title}</h1>
	</div>
</div>

<style>
	.page {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 98vh;
	}

	.container {
		background-color: rgb(28, 26, 38);
		padding: 0.5rem 2rem;
		border-radius: 15px;
		opacity: 98%;
		margin-bottom: 2rem;
		min-width: 300px;
		max-width: 900px;
		width: 100%;
	}
</style>
