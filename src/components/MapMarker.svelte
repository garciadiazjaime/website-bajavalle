<style>
	:global(.marker) {
		background-image: url('/mapbox-icon.png');
		background-size: cover;
		width: 50px;
		height: 50px;
		border-radius: 50%;
		cursor: pointer;
	}
</style>
<script>
	import { getContext } from 'svelte';
	import { mapbox, key } from '../support/mapbox.js';

	const { getMap } = getContext(key);
	const map = getMap();

	export let lat;
	export let lon;
	export let label;

	const popup = new mapbox.Popup({ offset: 25 })
		.setText(label);

	const el = document.createElement('div');
  el.className = 'marker';

	const marker = new mapbox.Marker(el)
		.setLngLat([lon, lat])
		.setPopup(popup)
		.addTo(map);
</script>
