<script lag="ts">
	import EntryList from './EntryList.svelte';
</script>

<div class="container">
	<h1>Tidigare bidrag</h1>
	<p>
		Here is a summary of the previous event. It was such a great time! Everyone laughed. I can't
		rememeber the last time so many people had so much fun. I think it's some kind of record. Here
		are some of the entries.
	</p>

	<h2>Tema: "Goda råd"</h2>

	<EntryList />
</div>

<style>
	h1 {
		font-size: 3rem;
		margin-bottom: 0;
	}
	.container {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		margin: 10rem 8rem 0 8rem;
	}

	p {
		margin: 1rem 0 3rem 0;
	}

	@media (max-width: 768px) {
		h1 {
			font-size: 1.8rem;
			margin-bottom: 0;
		}

		.container {
			text-align: center;
			margin: 10rem 1rem 0 1rem;
		}
	}
</style>
