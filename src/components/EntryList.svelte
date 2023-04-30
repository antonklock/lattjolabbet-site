<script>
	import EntryComponent from './EntryComponent.svelte';
</script>

<div class="container">
	<div class="entryRow">
		<EntryComponent
			heading="Goda Råd - Simon"
			creator="Simon"
			paragraph="This is entry number one's paragraph. This is entry number one's This is entry number one's paragraph. This is entry number one's paragraph. "
			image="https://images.unsplash.com/photo-1591025810539-a321000cda85?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1740&q=80"
			mediaSrc="/PreviousEntries/godRadSimon.mp3"
			type="audio"
			alt="A weird looking thing."
		/>
	</div>

	<div class="entryRow">
		<EntryComponent
			heading="Fånga dagen"
			creator="Erik Modin"
			paragraph="This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. "
			image="https://images.unsplash.com/photo-1618767451283-c9705dff0874?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1742&q=80"
			mediaSrc="/PreviousEntries/fanga-dagen.mp4"
			type="video"
			alt="A weird looking thing."
			color="blue"
		/>
	</div>

	<div class="entryRow">
		<EntryComponent
			heading="Entry #1"
			creator="Erik Modin"
			paragraph="This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. "
			image="https://images.unsplash.com/photo-1515144225933-899dcb0ca32e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80"
			mediaSrc="https://images.unsplash.com/photo-1515144225933-899dcb0ca32e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80"
			alt="A weird looking thing."
		/>
	</div>

	<div class="entryRow">
		<EntryComponent
			heading="Entry #1"
			creator="Joel Gerhardsson"
			paragraph="This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. "
			image="/thing_01.jpg"
			mediaSrc="/thing_01.jpg"
			alt="A weird looking thing."
			color="blue"
		/>
	</div>

	<div class="entryRow">
		<EntryComponent
			heading="Entry #1"
			creator="Joel Gerhardsson"
			paragraph="This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. This is entry number one's paragraph. "
			image="/thing_01.jpg"
			mediaSrc="/thing_01.jpg"
			alt="A weird looking thing."
		/>
	</div>
</div>

<style lang="scss">
	.container {
		width: 100%;
		display: flex;
		flex-direction: column;
	}

	.container .entryRow:nth-child(even) {
		display: flex;
		flex-direction: row;
		justify-content: flex-end;
	}

	@media (max-width: 768px) {
		.container {
			width: 100%;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}

		// .container .entryRow:nth-child(even) {
		// 	display: flex;
		// 	flex-direction: row;
		// 	justify-content: center;
		// 	align-items: center;
		// }

		// .container .entryRow:nth-child(odd) {
		// 	display: flex;
		// 	flex-direction: row;
		// 	justify-content: center;
		// 	align-items: center;
		// }
	}
</style>
