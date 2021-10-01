<style>
	.container {
		max-width: 1120px;
		margin: 0 auto;
	}

	.gallery {
		display: flex;		
	}

	img {
		object-fit: cover;
		vertical-align: bottom;
	}

	.gallery-grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
		grid-template-rows: 1fr;
	}

	img.gallery-cover {
		height: 568px;
		width: 560px;
		margin-right: 8px;
	}

	img.gallery-item {
		height: 280px;
		width: 272px;
	}

	.left-border {
		border-radius: 6px 0 0 6px;
	}

	.right-top-border {
		border-radius: 0 6px 0 0;
		margin-left: 8px;
	}

	.right-bottom-border {
		border-radius: 0 0 6px 0;
	}
	
	.margin-left {
		margin-left: 8px;
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
		.gallery {
			display: block;
		}

		.content {
			padding: 0 12px;
		}
		
		.gallery-grid {
			display: none;
		}

		img.gallery-cover, img.gallery-item {
			width: 375px;
			height: 250px;
			margin: 0;
			border-radius: 0;
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
	
	<div class="gallery">
		<img src="house/conejo/front-night.jpeg" alt="" class="gallery-cover left-border">

		<div class="gallery-grid">
			<img src="house/conejo/east-side.jpeg" alt="" class="gallery-item">
			<img src="house/conejo/entrance.jpeg" alt="" class="gallery-item right-top-border margin-left">
			<img src="house/conejo/west-side.jpeg" alt="" class="gallery-item">
			<img src="house/conejo/garden.jpeg" alt="" class="gallery-item right-bottom-border margin-left">
		</div>
	</div>
</div>
