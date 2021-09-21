<script>
  export let profileHeight
  export let handlerCloseProfile
  export let item
</script>

<style>
	.profile {
		position: absolute;
    bottom: 0;
    left: 0;
		background-color: white;
		width: 100%;
	}

	.close-btn {
		position: absolute;
    top: 0;
    right: 0;
    font-size: 26px;
	}
	.close-btn:hover {
		cursor: pointer;
	}
</style>

<div class="profile" style={`height: ${profileHeight}px`}>
  <div class="close-btn" on:click={handlerCloseProfile}>
    X
  </div>
  <div>
    {item.title}
  </div>
</div>
