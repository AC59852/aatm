<template>
  <section id="homeServices">
      <h3>Some Services</h3>
      <div class="homeServCon">
          <div class="homeService" v-for="homeService in homeServices" :key="homeService.id">
              <img :src="homeService.icon" :alt="'Icon for ' + homeService.heading">
              <div class="homeServiceContent">
                <h4>{{ homeService.heading }}</h4>
                <p>{{ homeService.desc }}</p>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    data() {
        return {
            homeServices: [
                {id: 1, icon: 'images/connect.svg', heading: 'Service 1', desc: 'because it is pain, but because occasionally circumstances occur in which toil and pain'},
                {id: 2, icon: 'images/comment.svg', heading: 'Service 2', desc: 'because it is pain, but because occasionally circumstances occur in which toil and pain'},
                {id: 3, icon: 'images/zap.svg', heading: 'Service 3', desc: 'because it is pain, but because occasionally circumstances occur in which toil and pain'},
                {id: 4, icon: 'images/checkmark.svg', heading: 'Service 4', desc: 'because it is pain, but because occasionally circumstances occur in which toil and pain'},
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
    #homeServices {
        margin-bottom: 15%;
    }

    #homeServices h3 {
        text-align: center;
        position: relative;
        font-family: 'Inter';
        font-size: 1.4em;
        margin-bottom: 12%;
        font-weight: 600;
    }

    #homeServices h3::after {
        position: absolute;
        color: black;
        background-color: rgb(255, 169, 119);
        width: 8%;
        height: 4px;
        content: "";
        left: 50%;
        top: 160%;
        transform: translateX(-50%);
    }


    .homeService {
        width: 86%;
        margin: 8% auto;
        display: flex;
    }

    .homeService img {
        width: 30px;
        padding: 0 3%;
        border: solid 3px rgba(255, 189, 151, 0.89);
        border-radius: 100vw;
        height: 55px;
        margin-right: 9%;
    }

    .homeService h4 {
        font-family: 'Inter';
        font-size: 1.2em;
        font-weight: 600;
    }

    .homeService div {
        display: flex;
        flex-direction: column;
        width: 70%;
    }

    .homeService p {
        font-family: 'Rubik';
        margin-top: 3%;
        font-size: 1em;
        line-height: 1.3em;
        letter-spacing: 0.1px;
        color: gray;
    }
</style>