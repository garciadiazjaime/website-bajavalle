<script>
	import { onMount } from 'svelte';

	let index = 1
	const totalImages = 9

	onMount(async () => {
		setInterval(() => {
			document.getElementById('container').classList.remove('fadein')
			setTimeout(() => {
				document.getElementById('container').classList.add('fadein')
				index = (index + 1) % totalImages
			}, 300)
		}, 7000)
	});
</script>

<style>
	img {
		position: absolute;
		left: 0;
		top: 0;
		width: 100%;
		height: 100%;
	}

	#container {
		opacity: 0;
	}

	.fadein {
		animation: fadeIn 7s;
	}
	@keyframes fadeIn {
		0% {opacity:0;}
		30% {opacity:1;}
		86% {opacity:1;}
		100% {opacity:0;}
	}
</style>

<svelte:head>
	<title>Baja Valley Retreat</title>
</svelte:head>

<div id="container" class="fadein">
	<img alt="Success Kid" src={`/images/image_${index}.jpeg`}>
</div>
