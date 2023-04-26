<script lang="ts">
	import ArrowIcon from './ArrowIcon.svelte';

	export let heading: string;
	export let creator: string;
	export let paragraph: string;
	export let image: string;
	export let alt: string;
	export let position: 'left' | 'right' = 'left';
	export let state: 'expanded' | 'collapsed' = 'collapsed';

	let shortParagraph: string = paragraph.substring(0, 60) + '...';
	let arrowDir: 'down' | 'up' = 'down';

	if (state === 'expanded') {
		arrowDir = 'up';
	} else {
		arrowDir = 'down';
	}
</script>

<div class="outer {position} {state}">
	<div class="inner">
		<div class="entry">
			<div class="entryContent">
				<div class="entryImage">
					<img src={image} {alt} />
				</div>
				<div class="entryText">
					<h2>{heading}</h2>
					<subtitle>{creator}</subtitle>
					{#if state === 'collapsed'}
						<p>{shortParagraph}</p>
					{:else}
						<p>{paragraph}</p>
					{/if}
				</div>
			</div>
			<div class="arrowIcon">
				<ArrowIcon rotate={arrowDir} />
			</div>
		</div>
	</div>
</div>

<style lang="scss">
	h2 {
		font-size: 2rem;
		font-weight: 700;
		margin: 0;
		margin-bottom: 0.2rem;
	}

	subtitle {
		font-size: 1rem;
		font-weight: 400;
		margin: 0;
		margin-bottom: 1rem;
		font-style: italic;
	}

	.entry {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		align-items: start;
		margin: 2rem 0;
		max-width: 50vw;
	}

	.outer {
		border-radius: 1.5rem;
		margin-top: 2rem;
		margin-bottom: 2rem;
		box-shadow: 0.5rem 0.5rem 0rem rgba(0, 0, 0, 0.15);
	}

	.inner {
		background-color: white;
		margin: 3px;
		border-radius: 1.25rem;
		padding: 0.5rem 2rem;
	}

	.left {
		transform: translateX(-#{15}vw);
		background: rgb(251, 40, 195);
		background: linear-gradient(180deg, rgba(251, 40, 195, 1) 0%, rgba(178, 0, 146, 1) 100%);
	}

	.right {
		transform: translateX(#{15}vw);
		background: rgb(14, 223, 243);
		background: linear-gradient(180deg, rgba(14, 223, 243, 1) 0%, rgba(22, 156, 141, 1) 100%);
	}

	//Are expanded and collapsed the same here?? Refactor?? ////
	.expanded {
		display: flex;
		flex-direction: row;
		align-items: center;
		margin-bottom: 20px;
	}

	.expanded .entry {
		display: flex;
		flex-direction: column;
		align-items: end;
	}

	.expanded .entryContent {
		display: flex;
		flex-direction: row;
		align-items: center;
	}

	.collapsed .entry {
		display: flex;
		flex-direction: column;
		align-items: end;
	}

	.collapsed .entryContent {
		display: flex;
		flex-direction: row;
		align-items: center;
		margin-bottom: 20px;
	}

	.entry .arrowIcon {
		height: 10px;
	}

	.collapsed .entryImage {
		display: flex;
		justify-content: center;
		padding-right: 20px;
	}

	.collapsed .entryImage img {
		height: 100px;
	}

	@media screen and (max-width: 768px) {
		.entry {
			max-width: 100vw;
		}

		.entry .entryContent {
			flex-direction: column;
			align-items: center;
		}

		.entry .entryImage {
			padding-right: 0px;
		}

		.entry .entryImage img {
			height: 200px;
		}

		.entry .entryText {
			text-align: center;
		}

		.left {
			transform: translateX(#{0}vw);
			margin: 0 2rem;
		}

		.right {
			transform: translateX(#{0}vw);
			margin: 2rem 2rem;
		}

		.collapsed .entry {
			display: flex;
			flex-direction: column;
			align-items: center;
		}
	}
</style>
