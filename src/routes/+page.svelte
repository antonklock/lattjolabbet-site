<script lang="ts">
	import Header from '../components/Header.svelte';
	import NextEvent from '../components/NextEvent.svelte';
	import PageDownArrow from '../components/PageDownArrow.svelte';
	import PreviousEntries from '../components/PreviousEntries.svelte';
	import EntryComponent from '../components/EntryComponent.svelte';
	import Footer from '../components/Footer.svelte';

	let screenSize: number = 0;
</script>

<svelte:window bind:innerWidth={screenSize} />

<div class="page">
	<div class="content-area">
		<Header />
		<PageDownArrow />
		<div class="next-event">
			<NextEvent />
			{#if screenSize > 1000}
				<div class="image">
					<img src="./thing_01.jpg" alt="A weird thing" />
				</div>
			{/if}
		</div>

		<PreviousEntries />

		<EntryComponent
			heading="Entry #1"
			creator="Anton Klock"
			paragraph="This is entry number one's paragraph. This is entry number one's... "
			image="/thing_01.jpg"
			alt="A weird looking thing."
		/>

		<EntryComponent
			heading="Entry #1"
			creator="Linda Zetterholm"
			paragraph="This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. "
			image="/thing_01.jpg"
			alt="A weird looking thing."
			position="right"
		/>

		<EntryComponent
			heading="Entry #1"
			creator="Erik Modin"
			paragraph="This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. "
			image="/thing_01.jpg"
			alt="A weird looking thing."
		/>

		<EntryComponent
			heading="Entry #1"
			creator="Joel Gerhardsson"
			paragraph="This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. "
			image="/thing_01.jpg"
			alt="A weird looking thing."
			position="right"
		/>

		<EntryComponent
			heading="Entry #1"
			creator="Joel Gerhardsson"
			paragraph="This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. "
			image="/thing_01.jpg"
			alt="A weird looking thing."
		/>

		<Footer />
	</div>
</div>

<style>
	div {
		font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
	}

	.next-event {
		display: flex;
		flex-direction: row;
		justify-content: space-around;
		align-items: center;
	}

	.next-event img {
		width: 75%;
		margin-left: 2rem;
	}

	.page {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.content-area {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		max-width: 1200px;
	}
</style>
