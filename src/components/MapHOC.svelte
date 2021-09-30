<script>
	import { onMount } from 'svelte';

	import Profile from '../components/Profile.svelte'
	import Map from '../components/Map.svelte';
	import MapMarker from '../components/MapMarker.svelte';

  export let items
  export let center

	let markerSelected

	let deviceHeight = 0
	let headerHeight = 0
	let mapHeight = 0

  function initHeights() {
    deviceHeight = document.documentElement.clientHeight
		headerHeight = document.querySelector('nav').offsetHeight

		mapHeight = deviceHeight - headerHeight
  }

  function showProfile(event) {
		markerSelected = event.detail.slug
  }

  function hideProfile() {
		markerSelected = null
  }

	onMount(async () => {
		initHeights()
	});
</script>

<div>
	<div style={`height: ${mapHeight}px`}>
		<Map lat={center.lat} lon={center.lon} zoom={center.zoom}>
      {#each Object.keys(items) as slug}
        <MapMarker lat={items[slug].lat} lon={items[slug].lon} slug={slug} on:markerClicked={showProfile}/>
      {/each}
		</Map>
	</div>

  {#if markerSelected}
    <Profile
      handlerCloseProfile={hideProfile}
      item={items[markerSelected]}
    />
  {/if}
</div>
