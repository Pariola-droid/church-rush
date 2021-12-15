<template>
  <header>
      <div class="wrapper">
            <div class="content">
                <h1>
                    Church Rising Up, Serving Him
                </h1>
                <p>
                    A safe place to grow in faith, have an encounter with God, find your community and fufill your purpose. Would you like us to notify you when we launch?
                </p>
                <button @click="$refs.modalName.openModal()">
                    Keep me in the loop
                </button>
            </div> 

            <div class="showoff">
                <img class="s-off1" :src="require('../../assets/show-off1.png')" alt="church rush show off - app"/>
                <img class="s-off2" :src="require('../../assets/show-off2.png')" alt="church rush show off - app"/>
            </div> 

            <modal ref="modalName">
                <template v-slot:header>
                    
                </template>

                <template v-slot:body>
                   
                </template>

                <template v-slot:footer>
                    <!-- <div class="d-flex align-items-center justify-content-between">
                    <button class="btn btn--secondary" @click="$refs.modalName.closeModal()">Cancel</button>
                    <button class="btn btn--primary" @click="$refs.modalName.closeModal()">Save</button>
                    </div> -->
                </template>
            </modal>
      </div>    
  </header>
</template>

<script>
import Modal from "../general/Modal.vue";

export default {
//   name: "App",
  components: {
    Modal
  }
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

@keyframes inf_show1 {
    0% {
        top: -70px;
    }

    100% {
        top: -80px;
    }
}
@keyframes inf_show2 {
    0% {
        top: 20px;
    }

    100% {
        top: 30px;
    }
}

header {
    height: fit-content;
    width: 100%;
    background: #311747;
    display: grid;
    place-items: center;
}

header .wrapper {
    height: fit-content;
    width: 1100px;
    background: #311747;
    margin: 0 auto;
    margin-top: 200px;
    margin-bottom: 200px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

/* content */

.wrapper .content {
    height: fit-content;
    width: fit-content;
    display: flex;
    align-items: flex-start;
    flex-direction: column;
}

.wrapper .content h1 {
    height: fit-content;
    max-width: 540px;
    margin: 16px 0px;
    font-style: normal;
    font-weight: 800;
    font-size: 64px;
    line-height: 98px;
    color: #FFFFFF;
}

.wrapper .content p {
    height: fit-content;
    max-width: 540px;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 32px;
    color: #FFFFFF;
    margin: 16px 0px;
}

.wrapper .content button {
    padding: 12px 32px;
    width: 225px;
    height: 58px;
    background: #FFCC00;
    border-radius: 6px;
    outline: 0;
    border: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 24px;
    text-align: center;
    color: #311747;
    font-family: 'Poppins', sans-serif;
    margin-top: 49px;
    cursor: pointer;
}


/* showoff */

.wrapper .showoff {
    height: 400px;
    width: 500px;
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    position: relative;
    /* background-color: #fff; */
}

.showoff .s-off1 {
    position: absolute;
    top: -80px;
    animation-name: inf_show1;
    animation-timing-function: ease-in;
    animation-duration: 1.5s;
    animation-fill-mode: forwards; 
    animation-delay: .5s; 
    animation-iteration-count: infinite;
    /* transition: 1s ease-in; */
}
.showoff .s-off2 {
    z-index: 99;
    position: absolute;
    right: -150px;
    top: 30px;
    animation-name: inf_show2;
    animation-timing-function: ease-in;
    animation-duration: 1.5s;
    animation-fill-mode: forwards; 
    animation-delay: 1s;  
    animation-iteration-count: infinite;
    /* transition: 1s ease-in; */
}

</style>