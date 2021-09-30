<script>
  import Carousel from "./Carousel.svelte"
  export let handlerCloseProfile
  export let item
</script>

<style>
	.profile {
		position: fixed;
    top: 0;
    left: 0;
		background-color: white;
		width: 100%;
    height: 100%;
    z-index: 3;
	}

	.close-btn {
		position: absolute;
    top: 0;
    right: 0;
    font-size: 26px;
    z-index: 1;
	}
	.close-btn:hover {
		cursor: pointer;
	}
</style>

<div class="profile">
  <div class="close-btn" on:click={handlerCloseProfile}>
    X
  </div>

  <Carousel images={item.images} />
  <h2>{item.title}</h2>
</div>
