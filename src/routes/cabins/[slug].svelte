<script>
  import Gallery from "../../components/Gallery.svelte"; 

  export let place = {}
	export let slug = ''
</script>

<script context="module">
	// the (optional) preload function takes a
	// `{ path, params, query }` object and turns it into
	// the data we need to render the page
	export async function preload(page, session) {
		// the `slug` parameter is available because this file
		// is called [slug].svelte
		const { slug } = page.params;

		const places = {
      'cabin-1': {
        name: 'Conejo Añejo',
        description: 'El muerto al pozo y el vivo al gozo.',
      },
      'cabin-2': {
        name: 'Conejo Parejo',
        description: 'Dando y dando, pajarito volando.',
      },
      'cabin-3': {
        name: 'Conejo Espejo',
        description: '¡A darle que es mole de olla!',
      },
    }

		return { place: places[slug], slug };
	}
</script>


<style>
	.container {
		max-width: 1120px;
		margin: 0 auto;
	}

  h1 {
		font-size: 26px;
		font-weight: 600;
		line-height: 30px;
		margin: 0;
		color: rgb(34, 34, 34);
	}

	h2 {
		font-size: 14px;
		font-weight: 600;
		color: rgb(113, 113, 113);
		margin: 12px 0 24px 0;
	}

	@media only screen and (max-width: 620px) {
		.content {
			padding: 0 12px;
		}
	}

  a {
    padding: 20px 42px;
    background-color: #DE3151;
    text-decoration: none;
    color: white;
    border-radius: 5px;
  }

  .reserve {
    width: 100%;
    text-align: center;
    margin-top: 40px;
  }
</style>

<div class="container">
  <div class="content">
		<h1>{place.name}</h1>
		<h2>{place.description}</h2>
	</div>

  <Gallery cabin={slug} />

  <div class="reserve">
    <a href="https://www.airbnb.com/" target="_blank">Reservar!</a>
  </div>
</div>
