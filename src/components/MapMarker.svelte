<script>
	import { getContext } from 'svelte';
	import { mapbox, key } from '../support/mapbox.js';
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	const { getMap } = getContext(key);
	const map = getMap();

	export let lat;
	export let lon;
	export let slug;

	const el = document.createElement('div');
  el.className = 'marker';
	el.addEventListener('click', () => {
		dispatch('markerClicked', {
			slug,
		});
	})

	const marker = new mapbox.Marker(el)
		.setLngLat([lon, lat])
		.addTo(map);
</script>

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
