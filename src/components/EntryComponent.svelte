<script lang="ts">
	import Icon from '@iconify/svelte';
	import ArrowIcon from './ArrowIcon.svelte';
	import { Modal, Content, Trigger } from 'sv-popup';

	export let heading: string;
	export let creator: string;
	export let paragraph: string;
	export let image: string;
	export let mediaSrc: string;
	export let alt: string;
	export let position: 'left' | 'right' = 'left';
	export let state: 'expanded' | 'collapsed' = 'collapsed';
	export let type: 'image' | 'video' | 'audio' = 'image';
	export let color: 'red' | 'blue' = 'red';

	let shortParagraph: string = paragraph.substring(0, 60) + '...';
	let arrowDir: 'down' | 'up' = 'down';

	if (state === 'expanded') {
		arrowDir = 'up';
	} else {
		arrowDir = 'down';
	}

	const handleCollapse = () => {
		if (state === 'expanded') {
			state = 'collapsed';
			arrowDir = 'down';
		} else {
			state = 'expanded';
			arrowDir = 'up';
		}
	};
</script>

<div
	class="outer {position} {state} {color}"
	on:click={() => handleCollapse()}
	on:keydown={() => handleCollapse()}
>
	<div class="inner">
		<div class="entry">
			<div class="entryContent">
				{#if state === 'collapsed'}
					<div class="entryImage">
						<img src={image} {alt} />
					</div>
					<div class="entryText">
						<h2>{heading}</h2>
						<subtitle>{creator}</subtitle>

						<p>{shortParagraph}</p>
					</div>
				{:else}
					<div class="entryImage">
						{#if type === 'image'}
							<Modal button={false} big={true}>
								<Content>
									<img src={mediaSrc} {alt} />
								</Content>
								<Trigger>
									<img src={image} {alt} />
								</Trigger>
							</Modal>
						{:else if type === 'video'}
							<div class="videoPlayer">
								<video width="450" src={mediaSrc} controls>
									<track kind="captions" />
								</video>
							</div>
						{:else if type === 'audio'}
							<img src={image} {alt} />
							<audio src={mediaSrc} controls />
						{/if}
					</div>
					<div class="entryText">
						<h2>{heading}</h2>
						<subtitle>{creator}</subtitle>

						<p>{paragraph}</p>
					</div>
				{/if}
			</div>
			<div class="arrowIcon" on:click={() => handleCollapse()} on:keydown={() => handleCollapse()}>
				<ArrowIcon rotate={arrowDir} />
			</div>
		</div>
	</div>
</div>

<style lang="scss">
	.shadow {
		text-shadow: 0.5rem 0.35rem 1rem rgba(0, 0, 0, 0.25);
	}

	h2 {
		font-size: 1.5rem;
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

	p {
		font-size: 0.85rem;
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
		margin: 2rem 1rem 2rem 1rem;
		box-shadow: 0.5rem 0.35rem 1rem rgba(0, 0, 0, 0.1);
		overflow: hidden;
		width: 75%;
	}

	.inner {
		background-color: white;
		margin: 3px;
		border-radius: 1.25rem;
		padding: 0.5rem 2rem;
		overflow: hidden;
	}

	.red {
		background: rgb(251, 40, 195);
		background: linear-gradient(180deg, rgba(251, 40, 195, 1) 0%, rgba(178, 0, 146, 1) 100%);
	}

	.blue {
		background: rgb(14, 223, 243);
		background: linear-gradient(180deg, rgba(14, 223, 243, 1) 0%, rgba(22, 156, 141, 1) 100%);
	}

	//Are expanded and collapsed the same here?? Refactor?? ////
	.expanded {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
	}

	.expanded .entry {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		margin: 2rem;
	}

	.expanded .entryContent {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.expanded .entryImage {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding-right: 20px;
		margin-bottom: 4rem;
	}

	.expanded .entryImage img {
		height: 200px;
	}

	.expanded video {
		border-radius: 1.25rem;
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
		position: relative;
		display: flex;
		justify-content: center;
		padding-right: 20px;
	}

	.collapsed .entryImage img {
		position: absolute;
		width: 300px;
		height: auto;
		transform: translateX(-50%) translateY(-50%);
	}

	@media screen and (max-width: 768px) {
		.outer {
			width: 90%;
			margin: 0, 2rem, 0, 2rem;
		}
		.entry {
			max-width: 100%;
		}

		.entry .entryContent {
			flex-direction: column;
			align-items: center;
		}

		.entry .entryImage {
			padding-right: 0px;
		}

		.entry .entryImage img {
			height: 100px;
			border-radius: 20px;
		}

		.entry .entryText {
			text-align: center;
		}

		.collapsed .entry {
			display: flex;
			flex-direction: column;
			align-items: center;
		}

		.collapsed .entryImage {
			position: relative;
			display: flex;
			justify-content: center;
			padding-right: 20px;
		}

		.collapsed .entryImage img {
			position: relative;
			width: 100px;
			height: auto;
			transform: translateX(0%) translateY(0%);
		}

		.expanded .entry {
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
			margin: 0rem 0rem 2rem 0rem;
		}

		.expanded video {
			width: 100%;
		}

		.expanded .entryImage {
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
			padding-right: 0px;
			margin: 1rem 0rem 1rem 0rem;
		}
	}
</style>
