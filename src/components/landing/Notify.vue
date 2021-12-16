<template>
  <div class="notify">
      <div class="wrapper">
            <div class="content">
                <h1>
                    Get notified when we launch.
                </h1>
                <button>
                    Notify me
                </button>
            </div> 
      </div>    
  </div>
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

.notify {
    height: fit-content;
    width: 100%;
    background: #fff;
    display: grid;
    place-items: center;
}

.notify .wrapper {
    /* height: 266px; */
    width: 1100px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 64px 165px;
}

/* content */

.wrapper .content {
    height: fit-content;
    width: fit-content;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;    
}

.wrapper .content h1 {
    font-style: normal;
    font-weight: 800;
    font-size: 40px;
    line-height: 54px;
    color: #311747;
    margin: 32px 0px;
}

.wrapper .content button {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 14px 24px;
    width: 113px;
    height: 52px;
    background: #FFCC00;
    border-radius: 8px;
    cursor: pointer;
    outline: 0;
    border: 0;
    font-family: 'Inter', sans-serif;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
    color: #311747;
}


/* Responsiveness */

/* 600px */

@media (max-width:600px) {

    .notify .wrapper {
        width: 100%;
        padding: 32px 20px;
    }

    .wrapper .content h1 {
        font-weight: 700;
        font-size: 20px;
        line-height: 34px;
        margin: 24px 0px;
    }

    .wrapper .content button {
        border-radius: 12px;
        font-weight: 400;
        font-size: 14px;
        line-height: 20px;
        color: #311747;
        padding: 8px 24px;
        width: 162px;
        height: 48px;
    }

}



</style>