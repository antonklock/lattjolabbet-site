<script lang="ts">
</script>

<div class="page">
	<img src="/lattjolabbet_background.jpg" alt="Lattjolabbet" class="background" />

	<div class="container">
		<h1>LATTJOLABBET</h1>
	</div>
	<div class="container">
		<h3>Datum</h3>
		<p>30/09/23</p>

		<h3>Plats</h3>
		<p>Östra Strandgatan 32</p>

		<h3>Tider</h3>
		<p>16:00 - Dörrarna öppnar</p>
		<p>17:30 - Tema-reveal</p>
		<p>20:00 - Cut off</p>
		<p>20:30 - Presentation av resultat</p>
		<p>Sent - Hemgång</p>
	</div>
</div>

<style>
	.background {
		background-color: black;
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
		z-index: -1;
		filter: blur(3px);
		opacity: 0.75;
	}

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
		max-width: 700px;
	}

	h1 {
		color: white;
		font-size: 2.5rem;
		text-align: center;
		font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
	}

	h3 {
		color: white;
		font-size: 1rem;
		text-align: left;
		font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
		margin-bottom: 0;
	}
	p {
		color: white;
		font-size: 0.7rem;
		text-align: left;
		font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
		margin-top: 0;
	}
</style>
