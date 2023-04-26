<script lang="ts">
</script>

<header>
	<!-- <h1>LATTJOLABBET</h1> -->
	<div class="title-container">
		<div class="title-parent">
			<h1 class="tbg-01 title-child-1">LAT</h1>
			<h1 class="shadow title-child-2">LAT</h1>
		</div>

		<div class="title-parent">
			<h1 class="tbg-02 title-child-1">TJO</h1>
			<h1 class="shadow title-child-2">TJO</h1>
		</div>

		<div class="title-parent">
			<h1 class="tbg-03 title-child-1">LAB</h1>
			<h1 class="shadow title-child-2">LAB</h1>
		</div>
		<div class="title-parent">
			<h1 class="tbg-04 title-child-1">BET</h1>
			<h1 class="shadow title-child-2">BET</h1>
		</div>
	</div>
</header>

<style>
	.title-parent {
		position: relative;
	}

	.title-child-1 {
		position: relative;
	}

	.title-child-2 {
		position: absolute;
		top: 0;
		left: 0;
	}

	.title-container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}

	h1 {
		color: black;
		font-size: 13vh;
		font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
		font-weight: 800;
		margin: 0;
		position: static;
	}

	.shadow {
		z-index: -1;
		text-shadow: 0.5rem 0.35rem 0rem rgba(0, 0, 0, 0.25);
	}

	.tbg-01 {
		background: url('/text-backgrounds/tbg_01.jpg') no-repeat center center;
		background-size: cover;
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	.tbg-02 {
		background: url('/text-backgrounds/tbg_02.jpg') no-repeat center center;
		background-size: cover;
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	.tbg-03 {
		background: url('/text-backgrounds/tbg_03.jpg') no-repeat center center;
		background-size: cover;
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	.tbg-04 {
		background: url('/text-backgrounds/tbg_04.jpg') no-repeat center center;
		background-size: cover;
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}
</style>
