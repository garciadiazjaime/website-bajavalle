<script>
	export let cabin
</script>

<style>
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

	@media only screen and (max-width: 620px) {
		.gallery {
			display: block;
		}
		
		.gallery-grid {
			display: block;
		}

		img.gallery-cover, img.gallery-item {
			width: 100%;
			max-height: 250px;
			margin: 0;
			border-radius: 0;
			margin-bottom: 20px;
		}
	}
</style>

<div class="gallery">
  <img src={`/cabins/${cabin}/front.webp`} alt="" class="gallery-cover left-border">

  <div class="gallery-grid">
    <img src={`/cabins/${cabin}/bedroom.webp`} alt="" class="gallery-item">
    <img src={`/cabins/${cabin}/livingroom.webp`} alt="" class="gallery-item right-top-border margin-left">
    <img src={`/cabins/${cabin}/kitchen.webp`} alt="" class="gallery-item">
    <img src={`/cabins/${cabin}/garden.webp`} alt="" class="gallery-item right-bottom-border margin-left">
  </div>
</div>
