<script>
	import Map from '../components/MapHOC.svelte';

	const center = {
		lat: 32.028019,
		lon: -116.6330805,
		zoom: 11,
	}
	const items = {
		"baja-valle-retreat": {
			title: "Baja Valley Retreat",
			lat: 32.028019,
			lon: -116.6330805,
		}
	}
</script>

<svelte:head>
	<title>Baja Valley Retreat</title>
</svelte:head>

<Map items={items} center={center} />
