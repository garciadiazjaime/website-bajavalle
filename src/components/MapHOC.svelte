<script>
	import { onMount } from 'svelte';

	import Profile from '../components/Profile.svelte'
	import Map from '../components/Map.svelte';
	import MapMarker from '../components/MapMarker.svelte';

  export let items
  export let center

	let markerSelected

	const smallMapHeight = 200
	let deviceHeight = 0
	let headerHeight = 0
	let containerHeight = 0
	let mapHeight = 0
	let profileHeight = 0

	let triggerResize = 0

  function initHeights() {
    deviceHeight = document.documentElement.clientHeight
		headerHeight = document.querySelector('nav').offsetHeight

		containerHeight = deviceHeight - headerHeight
		mapHeight = containerHeight
		profileHeight = deviceHeight - headerHeight - smallMapHeight
  }

  function showProfile(event) {
    mapHeight = smallMapHeight
		markerSelected = event.detail.slug
		triggerResize += 1
  }

  function hideProfile() {
    mapHeight = containerHeight
		markerSelected = null
		triggerResize += 1
  }

	onMount(async () => {
		initHeights()
	});
</script>

<div style={`height: ${containerHeight}px`}>
	<div style={`height: ${mapHeight}px`}>
		<Map lat={center.lat} lon={center.lon} zoom={center.zoom} triggerResize={triggerResize}>
      {#each Object.keys(items) as slug}
        <MapMarker lat={items[slug].lat} lon={items[slug].lon} slug={slug} on:markerClicked={showProfile}/>
      {/each}
		</Map>
	</div>

  {#if markerSelected}
    <Profile
      profileHeight={profileHeight}
      handlerCloseProfile={hideProfile}
      item={items[markerSelected]}
    />
  {/if}
</div>
