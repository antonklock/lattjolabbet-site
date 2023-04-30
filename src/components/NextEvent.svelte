<script lang="ts">
</script>

<div class="outer">
	<div class="inner">
		<div class="content">
			<div class="info">
				<h1>Nästa event</h1>
				<h3>Datum</h3>
				<p>7e maj 2023</p>

				<h3>Plats</h3>
				<p>Östra Strandgatan 32</p>

				<h3>Tider</h3>
				<p><strong>16:00</strong> - Dörrarna öppnar</p>
				<p><strong>17:30</strong> - Tema-reveal</p>
				<p><strong>20:00</strong> - Cut off</p>
				<p><strong>20:30</strong> - Presentation av resultat</p>
				<p><strong>Sent</strong> - Hemgång</p>
			</div>
		</div>
	</div>
</div>

<style>
	.outer {
		max-width: 100%;
		background: rgb(14, 223, 243);
		background: linear-gradient(180deg, rgba(14, 223, 243, 1) 0%, rgba(22, 156, 141, 1) 100%);
		border-radius: 1.5rem;
		display: flex;
		align-items: center;
		justify-content: center;

		box-shadow: 0.5rem 0.35rem 1rem rgba(0, 0, 0, 0.1);
	}

	.inner {
		background-color: white;
		margin: 3px;
		border-radius: 1.25rem;
	}

	.content {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		margin: 0rem 2rem;
		font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
	}

	.info {
		display: flex;
		flex-direction: column;
		justify-content: start;
		align-items: start;
		background-color: white;
		padding: 0.5rem 2rem;
		border-radius: 15px;
		margin-bottom: 2rem;
	}

	h1 {
		color: rgb(28, 26, 38);
		font-size: 2.4rem;
		font-weight: 800;
		text-align: Left;
		font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
		margin-bottom: 0;
	}

	h3 {
		color: rgb(28, 26, 38);
		font-size: 1.5rem;
		margin-top: 1rem;
		margin-bottom: 0;
	}

	p {
		color: rgb(28, 26, 38);
		font-size: 1rem;
		margin-top: 0;
		margin-bottom: 0;
	}

	@media (max-width: 768px) {
		.content {
			flex-direction: column;
			justify-content: start;
			align-items: start;
			width: 70vw;
			margin: 0rem 2rem;
			font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
		}

		.info {
			display: flex;
			flex-direction: column;
			justify-content: start;
			align-items: start;
			background-color: white;
			padding: 0.5rem 2rem;
			border-radius: 15px;
			margin-bottom: 2rem;
			max-width: 90vw;
		}

		h1 {
			color: rgb(28, 26, 38);
			font-size: 2rem;
			font-weight: 800;
			text-align: start;
			font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
			margin-bottom: 0;
		}

		h3 {
			color: rgb(28, 26, 38);
			font-size: 1.2rem;
			margin-top: 0.5rem;
			margin-bottom: 0;
		}

		p {
			color: rgb(28, 26, 38);
			font-size: 0.9rem;
			margin-top: 0;
			margin-bottom: 0;
		}
	}
</style>
