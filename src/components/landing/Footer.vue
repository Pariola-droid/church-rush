<template>
  <footer>
      <div class="wrapper">
            <div class="logo">
                <img :src="require('../../assets/ch-rush-logo.svg')" alt="church rush logo"/>
            </div>

            <div class="brand">
                © 2020 Regnify.  All rights reserved
            </div>

            <ul class="social">
                <li>fb</li>
                <li>tw</li>
                <li>ig</li>
            </ul>
      </div>    
  </footer>
</template>

<script>
// import logo from '../../assets/logo.png'
// export default {
//   name: 'HelloWorld',
//   props: {
//     msg: String
//   }
// }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

footer {
    height: fit-content;
    width: 100%;
    display: grid;
    place-items: center;
    background: #311747;
}

footer .wrapper {
    height: 72px;
    width: 1100px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.wrapper .brand {
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 24px;
    color: #D9DBE1
}

.wrapper .social {
    display: flex;
    align-items: center;
    justify-content: flex-start;
    margin: 0 16px;
}
.wrapper .social li {
    margin: 0 16px;
}




</style>