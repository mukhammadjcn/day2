<template>
  <div class="home">
    <Header />
    <intro/>
    <features/>
  </div>
</template>

<script>
import Features from '../components/Features.vue'
import Header from '../components/Header.vue'
import Intro from '../components/Intro.vue'


export default {
  name: 'Home',
  components: {
    Header,
    Intro,
    Features,
  },

  
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500;700;900&display=swap');

*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  list-style-type: none;
  text-decoration-line: none;
  font-family: 'Roboto', sans-serif;
}
#tsparticles{
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
  left: 0;
  .tsparticles-canvas-el{
    background-color: transparent !important;
  }
}
.row{
  display: flex;
  align-items: center;
}

.container{
  max-width: 1120px;
  margin: auto;
}
.title{
  font-weight: 900;
  font-size: 30px;
  line-height: 37px;
  text-align: center;
  text-transform: uppercase;
  color: #000000;
}

.info{
  font-weight: 500;
  font-size: 20px;
  line-height: 24px;
  text-align: center;
  color: #000000;
}
.minInfo{
  font-weight: 300;
  font-size: 14px;
  line-height: 16px;
  color: #000000;
}


@media (max-width:776px) {
  .container{
    max-width: 90%;
  }
}
</style>
