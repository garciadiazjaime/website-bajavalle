<script>
	import Gallery from "../components/Gallery.svelte"; 
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
</style>


<svelte:head>
	<title>Baja Valley Retreat</title>
</svelte:head>

<div class="container">
	<div class="content">
		<h1>100 Conejos</h1>
		<h2>Valle de Guadalupe, Baja California, Mexico</h2>
	</div>
	
	<Gallery />
</div>
