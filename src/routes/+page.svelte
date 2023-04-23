<script lang="ts">
	import Header from '../components/Header.svelte';
	import Footer from '../components/Footer.svelte';
	import SiteContent from '../components/SiteContent.svelte';
	import NextEvent from '../components/NextEvent.svelte';
	import PageDownArrow from '../components/PageDownArrow.svelte';
	import ContentContainer from '../components/ContentContainer.svelte';
	import PreviousEntries from '../components/PreviousEntries.svelte';

	let screenSize: number = 0;
</script>

<svelte:window bind:innerWidth={screenSize} />

<div class="page">
	<!-- <img src="/lattjolabbet_background.jpg" alt="Lattjolabbet" class="background" /> -->

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
		<!-- <SiteContent /> -->
		<!-- <Footer /> -->
	</div>
</div>

<style>
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

	.content-area {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
	.page {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
</style>
