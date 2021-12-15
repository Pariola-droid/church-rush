<template>
  <nav>
      <div class="nav_wrap">
        <div class="logo">
            <img :src="require('../../assets/ch-rush-logo.svg')" alt="church rush logo">
        </div>

        <ul class="list">
            <li>Features</li>
            <li>Roadmap</li>
            <li>Contact us</li>
        </ul>

        <div class="hmb">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M16 18V20H5V18H16ZM21 11V13H3V11H21ZM19 4V6H8V4H19Z" fill="#FAFAFA"/>
            </svg>
        </div>
      </div>   
  </nav>
</template>

<script>
// import './styles/navbar.scss'
// export default {
//   name: 'HelloWorld',
//   props: {
//     msg: String
//   }
// }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

@keyframes nav_nime {
    to {
        top: 0;
    }
}

nav {
    height: 100px;
    width: 100%;
    position: absolute;
    top: -100px;
    left: 0;
    display: grid;
    place-items: center;
    z-index: 99999;
    animation-name: nav_nime;
    animation-timing-function: ease-in;
    animation-duration: .8s;
    animation-fill-mode: forwards;  
}

nav .nav_wrap {
    height: 100%;
    width: 1100px;
    /* background: #fff; */
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.nav_wrap .logo {

}

.nav_wrap .hmb {
  display: none;
  cursor: pointer;
}

.nav_wrap .list {
  display: flex;
  align-items: center;
  justify-content: flex-start;
}

.nav_wrap .list li{
  margin-right: 32px;
  text-transform: capitalize;
  color: #fff;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
}

/* Responsiveness */

/* 600px */

@media (max-width:600px) {

  nav .nav_wrap {
      width: 88%;
  }

  .nav_wrap .hmb {
    display: initial;
  }

  .nav_wrap .list {
    display: none;
  }
}


</style>