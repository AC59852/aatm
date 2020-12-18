<template>
  <div class="home">
    <Hero />
    <section id="homeAbout" class="homePara">
      <h4>About Us?</h4>
      <h3>Example Heading <br> With Catchy Tag Lines <br> That Overlap</h3>
      <p>But I must explain to you how all this mistaken idea of denouncing pleasure and praising pain was born and I will give you a complete account of the system.</p>
      <router-link to="/about">Read More</router-link>
    </section>
    <HomeServices />
    <section id="homeClients" class="homePara">
      <h4>Our Clients?</h4>
      <h3>Something About <br> The Clients We Have <br> We Like Them</h3>
      <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptatibus eum nihil animi consectetur officiis? Ipsum repellendus eos voluptatem,</p>
      <router-link to="/clients">See More</router-link>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import Hero from '@/components/Hero.vue'
import HomeServices from '@/components/HomeServices.vue'

export default {
  name: 'Home',
  components: {
    Hero: Hero,
    HomeServices: HomeServices
  }
}
</script>

<style>
/* 
font-family: 'Inter', sans-serif;
font-family: 'Rubik', sans-serif; 
*/

  #homeAbout {
    margin-top: -5%;
  }

  .home {
    padding-bottom: 15%;
  }

  .homePara {
    width: 85%;
    margin: 0 auto 20%;
  }

  .homePara h3 {
    font-family: 'Inter';
    font-weight: 500;
    font-size: 1.9em;
    letter-spacing: 1px;
    line-height: 1.3em;
  }

  .homePara h4 {
    font-family: 'Inter';
    font-weight: 500;
    letter-spacing: 0.3px;
    color: rgb(255, 169, 119);
    font-size: 1.1em;
  }

  .homePara p {
    margin: 4% 0 6%;
    font-family: 'Rubik';
    width: 90%;
    line-height: 1.1em;
    font-size: 0.92em;
  }

  .homePara a {
    font-family: 'Rubik';
    font-weight: 500;
    color: black;
    text-decoration: none;
    border-bottom: solid 3px rgb(255, 169, 119);
    padding-bottom: 1%;
  }
</style>
