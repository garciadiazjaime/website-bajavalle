<style>
  a {
    text-decoration: none;
  }

  .intro {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    column-gap: 20px;
  }
  .intro div {
    gap: 10px;
    cursor: pointer;
  }
  
  img {
    width: 100%;
    height: auto;
    display: block;
    border-radius: 5px 5px 0 0;
    min-height: 240px;
    object-fit: cover;
  }

  .place {
    color: white;
    padding: 24px 12px;
    border-radius: 0px 0px 5px 5px;
    padding-bottom: 132px;
  }

  .color-1 {
    background-color: #DE3151;
  }

  .color-2 {
    background-color: #d93b30;
  }

  .color-3 {
    background-color: #bd196d;
  }

  @media only screen and (max-width: 620px) {
    .intro {
      display: block;
    }

    .intro div {
      margin-bottom: 40px;
    }

    img {
      border-radius: initial;
    }

    .place {
      border-radius: initial;
    }
  }
</style>

<div class="intro">
  <a href="./cabins/cabin-1">
    <picture>
      <source type="image/webp" srcset="/cabins/cabin-1/front.webp">
      <img src="/cabins/cabin-1/front.jpg" alt="">
    </picture>
    <div class="place color-1">
      <h2>Conejo Añejo</h2>
      <p>El muerto al pozo y el vivo al gozo.</p>
    </div>
  </a>
  <a href="./cabins/cabin-2">
    <picture>
      <source type="image/webp" srcset="/cabins/cabin-2/bedroom.webp">
      <img src="/cabins/cabin-2/bedroom.jpg" alt="">
    </picture>
    <div class="place color-2">
      <h2>Conejo Espejo</h2>
      <p>¡A darle que es mole de olla!</p>
    </div>
  </a>
  <a href="./cabins/cabin-3">
    <picture>
      <source type="image/webp" srcset="/cabins/cabin-3/kitchen.webp">
      <img src="/cabins/cabin-3/kitchen.jpg" alt="">
    </picture>
    <div class="place color-3">
      <h2>Conejo Parejo</h2>
      <p>Dando y dando, pajarito volando</p>
    </div>
  </a>
</div>
