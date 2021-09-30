<script>
	import Map from '../components/MapHOC.svelte';

	const center = {
		lat: 32.028019,
		lon: -116.6330805,
		zoom: 9,
	}
	const items = {
		"baja-valle-retreat": {
			title: "Baja Valley Retreat",
			lat: 32.028019,
			lon: -116.6330805,
			images: [
				'house/conejo/front-night.jpeg',
				'house/conejo/west-side.jpeg',
				'house/conejo/east-side.jpeg',
				'house/conejo/entrance.jpeg',
				'house/conejo/front-inside.jpeg',
				'house/conejo/garden.jpeg',
				'house/conejo/sky.jpeg',
				'house/conejo/terrace.jpeg',
			]
		}
	}
</script>

<svelte:head>
	<title>Baja Valley Retreat</title>
</svelte:head>

<Map items={items} center={center} />
