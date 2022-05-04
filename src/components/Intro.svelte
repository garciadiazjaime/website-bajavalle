<style>
  a {
    text-decoration: none;
  }

  .intro {
    display: flex;
    column-gap: 20px;
    align-items: center;
    justify-content: center;
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
  <a href="./cabana/conejo-este">
    <img src="house/conejo/east-side.jpeg" alt="">
    <div class="place color-1">
      <h2>Conejo Añejo</h2>
      <p>El muerto al pozo y el vivo al gozo.</p>
    </div>
  </a>
  <a href="./cabana/conejo-centro">
    <img src="house/conejo/entrance.jpeg" alt="">
    <div class="place color-2">
      <h2>Conejo Espejo</h2>
      <p>¡A darle que es mole de olla!</p>
    </div>
  </a>
  <a href="./cabana/conejo-oeste">
    <img src="house/conejo/west-side.jpeg" alt="">
    <div class="place color-3">
      <h2>Conejo Parejo</h2>
      <p>Dando y dando, pajarito volando</p>
    </div>
  </a>
</div>
