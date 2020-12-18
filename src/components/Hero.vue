<template>
  <section id="hero">
      <div class="heroImage">
          <div class="heroTitle">
            <h1>Ask A Tool Maker</h1>
            <h2>Bridging the Gap</h2>
          </div>
      </div>
      <div class="heroLogoCon">
          <div v-for="heroLogo in heroLogos" :key="heroLogo.id" class="heroLogo">
              <img :src="heroLogo.img" :alt="'Logo for ' + heroLogo.name">
          </div>
      </div>
  </section>
</template>

<script>
export default {
    data() {
        return {
            heroLogos: [
                {id: 1, name: 'Logo One', img: './images/apple.svg'},
                {id: 2, name: 'Logo Two', img: './images/facebook.svg'},
                {id: 3, name: 'Logo Three', img: './images/linkedin.svg'},
                {id: 4, name: 'Logo Four', img: './images/google.svg'},
                {id: 5, name: 'Logo Five', img: './images/github.svg'},
                {id: 6, name: 'Logo Six', img: './images/instagram.svg'},
                {id: 7, name: 'Logo Seven', img: './images/amazon.svg'},
                {id: 8, name: 'Logo Eight', img: './images/microsoft.svg'},
            ]
        }
    }
}
</script>

<style>
/* 
font-family: 'Inter', sans-serif;
font-family: 'Rubik', sans-serif; 
*/
    .heroImage {
        width: 100%;
        height: 30vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        position: relative;
    }

    .heroImage::before {
        position: absolute;
        content: "";
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: url("../../public/images/hero.jpg");
        filter: brightness(0.5);
    } 

    .heroTitle {
        position: relative;
    }

    .heroImage h1, .heroImage h2 {
        color: white;
        text-align: center;
    }

    .heroImage h1 {
        font-family: 'Inter';
        font-weight: 500;
        font-size: 2.4em;
        margin-bottom: 5%;
    }

    .heroImage h2 {
        font-family: 'Rubik';
        font-size: 1.4em;
    }

    .heroLogoCon {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        margin: 5% auto 14%;
        width: 90%;
    }

    .heroLogoCon div {
        width: 10%;
        margin: 2% 7% 5%;
    }

    .heroLogoCon div img {
        width: 100%;
    }
</style>