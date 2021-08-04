<template>
  <div class="home">
    <Header />
    <intro :option="option"/>
    <features/>
    <offer :option="option"/>
    <payments/>
    <services/>
    <partners/>
    <contact :option="option"/>
    <Footer/>

  </div>
</template>

<script>
import Contact from '../components/Contact.vue'
import Features from '../components/Features.vue'
import Footer from '../components/Footer.vue'
import Header from '../components/Header.vue'
import Intro from '../components/Intro.vue'
import Offer from '../components/Offer.vue'
import Partners from '../components/Partners.vue'
import Payments from '../components/Payments.vue'
import Services from '../components/Services.vue'



export default {
  name: 'Home',
  components: {
    Header,
    Intro,
    Features,
    Offer,
    Payments,
    Services,
    Partners,
    Contact,
    Footer,
  },
  data(){
        return{
            option : {
                        background: {
                            color: {
                                value: '#0d47a1'
                            }
                        },
                        fpsLimit: 60,
                        interactivity: {
                            detectsOn: 'canvas',
                            events: {
                                onClick: {
                                    enable: true,
                                    mode: 'push'
                                },
                                onHover: {
                                    enable: true,
                                    mode: 'repulse'
                                },
                                resize: true
                            },
                            modes: {
                                bubble: {
                                    distance: 400,
                                    duration: 2,
                                    opacity: 0.8,
                                    size: 40
                                },
                                push: {
                                    quantity: 4
                                },
                                repulse: {
                                    distance: 200,
                                    duration: 0.4
                                }
                            }
                        },
                        particles: {
                            color: {
                                value: '#ffffff'
                            },
                            links: {
                                color: '#ffffff',
                                distance: 150,
                                enable: true,
                                opacity: 0.5,
                                width: 1
                            },
                            collisions: {
                                enable: true
                            },
                            move: {
                                direction: 'none',
                                enable: true,
                                outMode: 'bounce',
                                random: false,
                                speed: 6,
                                straight: false
                            },
                            number: {
                                density: {
                                    enable: true,
                                    value_area: 800
                                },
                                value: 80
                            },
                            opacity: {
                                value: 0.5
                            },
                            shape: {
                                type: 'circle'
                            },
                            size: {
                                random: true,
                                value: 5
                            }
                        },
                        detectRetina: true
                    }
            }
    }
  
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


@media (max-width:1100px) {
  .container{
    max-width: 90%;
  }
}
</style>
