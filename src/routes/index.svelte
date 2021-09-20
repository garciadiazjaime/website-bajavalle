<script>
	import { onMount } from 'svelte';

	import Map from '../components/Map.svelte';
	import MapMarker from '../components/MapMarker.svelte';

	let mapHeight = 0

	onMount(async () => {
		const deviceHeight = document.documentElement.clientHeight
		const headerHeight = document.querySelector('nav').offsetHeight
		mapHeight = deviceHeight - headerHeight
	});
</script>

<style>
</style>

<svelte:head>
	<title>Baja Valley Retreat</title>
</svelte:head>

<div style={`height: ${mapHeight}px`}>
	<Map lat={32.028019} lon={-116.6330805} zoom={11}>
		<MapMarker lat={32.028019} lon={-116.6330805} label="Baja Valle Retreat"/>
	</Map>
</div>
