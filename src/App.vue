<template>
  <div id="app">
    <Navbar />
    <main>
      <Header />
      <FeaturesCH />
      <FeaturesLI />
      <Roadmap />
      <RoadMobile />
      <Notify />
    </main>
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/general/Navbar.vue'
import Header from './components/landing/Header.vue'
import FeaturesCH from './components/landing/FeaturesCH.vue'
import FeaturesLI from './components/landing/FeaturesLI.vue'
import Roadmap from './components/landing/Roadmap.vue'
import RoadMobile from './components/landing/RoadMobile.vue'
import Notify from './components/landing/Notify.vue'
import Footer from './components/landing/Footer.vue'

export default {
  name: 'app',
  components: {
    Navbar,
    Header,
    FeaturesCH,
    FeaturesLI,
    Roadmap,
    RoadMobile,
    Notify,
    Footer
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@200;300;400;500;600;800&family=Josefin+Sans:ital,wght@0,400;0,500;0,600;0,700;1,300&family=Mochiy+Pop+One&family=Poppins:wght@200;300;400;500;600;700;800;900&display=swap');


  *{
    box-sizing: border-box;
    padding: 0;
    list-style-type: none;
    text-decoration: none;
  }

  ::selection{
    background: #0f0f0f75;
    color: white;
  }


  html{
    scroll-behavior: smooth;
  }

  body {
    font-family: "Poppins", sans-serif;
    line-height: 17.38px;
    margin: 0;
    position: relative;
    overflow-x: hidden;
    background-color: #000;
    /* background-color: #0f0f0f; */

  }

  .overflow-hidden {
    overflow: hidden;
  }

  input[type=number]::-webkit-inner-spin-button {
    opacity: 0;
    display: none;
  }

  a {
      -webkit-transition-duration: 300ms;
      transition-duration: 300ms;
      -webkit-transition-property: opacity, color, background-color, -webkit-transform, border;
      -webkit-transition-property: opacity, color, background-color, transform, border;
      transition-property: opacity, color, background-color, transform, border;
    }

  h1,h2,h3,h4,h5,h6 {
    margin-block-start: 0em;
      margin-block-end: 0em;
  }

  figure {
      margin-block-start: 0em;
      margin-block-end: 0em;
      margin-inline-start: 0px;
      margin-inline-end: 0px;
  }

  input:-internal-autofill-selected {
      background-color: rgb(255, 255, 255) !important;
  }

  .st0{fill-rule:evenodd;clip-rule:evenodd;fill:#633001;}
  .st2{fill-rule:evenodd;clip-rule:evenodd;fill:#D1884F;}
  .st3{fill:#633001;}
  .st1{fill:#FEDC90;}
</style>
