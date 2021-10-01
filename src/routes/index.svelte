<style>
	.container {
		max-width: 1120px;
		margin: 0 auto;
	}

	.gallery {
		display: flex;		
	}

	.gallery-cover {
		margin-right: 8px;
	}

	img {
		object-fit: cover;
		vertical-align: bottom;
	}

	.gallery-cover img {
		height: 568px;
		width: 560px;
	}

	.gallery-items img {
		height: 280px;
		width: 272px;
	}

	.gallery-row {
		display: flex;
	}

	.gallery-row img:first-of-type {
		margin-right: 8px;
	}

	.gallery-row:first-of-type img{
		margin-bottom: 8px;
	}

	.left-border {
		border-radius: 6px 0 0 6px;
	}
</style>


<svelte:head>
	<title>Baja Valley Retreat</title>
</svelte:head>

<div class="container">

	<h1>Baja Valley Retreat</h1>
	<h2>Valle de Guadalupe, Baja California, Mexico</h2>
	
	<div class="gallery">
		<div class="gallery-cover">
			<img src="house/conejo/front-night.jpeg" alt="" class="left-border">
		</div>
		<div class="gallery-items">
			<div class="gallery-row">
				<img src="house/conejo/west-side.jpeg" alt="">
				<img src="house/conejo/east-side.jpeg" alt="">
			</div>
			
			<div class="gallery-row">
				<img src="house/conejo/entrance.jpeg" alt="">
				<img src="house/conejo/front-inside.jpeg" alt="">
			</div>
		</div>
	</div>
	
</div>
