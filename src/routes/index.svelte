<script>
	import Intro from "../components/Intro.svelte"

	function clickMapHandler() {
		console.log('clickMapHandler')
		window.open("https://goo.gl/maps/jop1FnZQjb1kPVKT8", "_blank")
	}
</script>

<style>
	.container {
		max-width: 1120px;
		margin: 0 auto;
	}

	h1 {
		font-size: 26px;
		font-weight: 600;
		line-height: 30px;
		margin: 0;
		color: rgb(34, 34, 34);
	}

	h2 {
		font-size: 14px;
		font-weight: 600;
		color: rgb(113, 113, 113);
		margin: 12px 0 24px 0;
	}

	@media only screen and (max-width: 620px) {
		.content {
			padding: 0 12px;
		}
	}

	.map {
		margin: 100px 0;
	}

	.map img {
		width: 100%;
		border-radius: 5px;
		cursor: pointer;
	}
</style>


<svelte:head>
	<title>Baja Valley Retreat</title>
</svelte:head>

<div class="container">
	<div class="content">
		<h1>¿Cuánto tiempo es para siempre?</h1>
		<h2>A veces, sólo un segundo.</h2>
	</div>
	
	<Intro />

	<div class="map">
		<img src="map.png" alt="Ubicación de Baja Valle Retreat" on:click={clickMapHandler}/>
	</div>
</div>
