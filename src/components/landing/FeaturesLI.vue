<template>
  <div class="featuresCH">
      <div class="wrapper">        
            <div class="content">
                <h1>
                    As a<br/> Listener
                </h1>

                <p>
                    A safe place to grow in faith, have an encounter with God, find your community and fulfil your purpose.
                </p>

                <ul class="list">
                    <li>
                        <svg width="10" height="10" viewBox="0 0 10 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <circle cx="5" cy="5" r="5" fill="#311747"/>
                        </svg>
                        Find your faith communities
                    </li>
                    <li>
                        <svg width="10" height="10" viewBox="0 0 10 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <circle cx="5" cy="5" r="5" fill="#311747"/>
                        </svg>
                        Experience Delightful Devotions
                    </li>
                    <li>
                        <svg width="10" height="10" viewBox="0 0 10 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <circle cx="5" cy="5" r="5" fill="#311747"/>
                        </svg>
                        Keep all your important notes
                    </li>
                    <li>
                        <svg width="10" height="10" viewBox="0 0 10 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <circle cx="5" cy="5" r="5" fill="#311747"/>
                        </svg>
                        Grow in faith with other believers
                    </li>
                </ul>
            </div> 

            <div class="display">
                <div class="inner">
                    <img data-aos="fade-up" data-aos-duration="3000" :src="require('../../assets/display2.png')" alt="church rush for listeners"/>
                </div> 
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

.featuresCH {
    height: fit-content;
    width: 100%;
    background: #fff;
    display: grid;
    place-items: center;
}

.featuresCH .wrapper {
    height: fit-content;
    width: 1100px;
    margin: 0 auto;
    margin-top: 52px;
    margin-bottom: 52px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    /* flex-wrap: wrap;     */
}


/* content */

.wrapper .content {
    height: fit-content;
    width: fit-content;
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    margin-right: 120px;
}

.content h1 {
    height: fit-content;
    max-width: 309px;
    font-style: normal;
    font-weight: 800;
    font-size: 48px;
    line-height: 64px;
    color: #18191F;
    /* margin: 24px 0px; */
}

.content p {
    height: fit-content;
    max-width: 442px;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 32px;
    color: #18191F;
    font-weight: 400;
}

.content .list {
    
}

.content .list li{
    /* margin: 0px 8px; */
    font-family: 'Inter', sans-serif;
    font-style: normal;
    font-weight: 600;
    font-size: 24px;
    line-height: 32px;
    color: #18191F;
    display: flex;
    align-items: center;
    justify-content: flex-start;
}

.content .list li svg{
    margin-right: 8px;
}

.content .list li:not(:last-of-type){
    margin-bottom: 40px;
}


/* showoff */
    
.wrapper .display {
    height: 600px;
    width: 600px;
    display: grid;
    place-items: center;
    border-radius: 100%;
    /* background: rgba(100, 25, 161, 0.2); */
}

.display .inner {
    height: 540px;
    width: 540px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgba(184, 142, 218, .2);
    border-radius: 100%;
    padding-top: 50px;
    overflow: hidden;
}


/* Responsiveness */

/* 600px */

@media (max-width:600px) {

    .featuresCH .wrapper {
        width: 88%;
        margin-top: 30px;
        justify-content: center; 
        flex-direction: column-reverse; 
    }

    /* showoff */
    
    .wrapper .display {
        height: 260px;
        width: 260px;
        margin-bottom: 40px;
        /* background: rgba(100, 25, 161, 0.2); */
    }

    .display .inner {
        height: 235px;
        width: 235px;
    }

    .display .inner img {
        transform: scale(.48);
    }

    /* content */

    .wrapper .content {
        align-items: center;
        justify-content: center;
        margin-right: 0;
    }

    .content h1 {
        text-align: center;
        font-weight: 700;
        font-size: 35px;
        line-height: 1.5;
    }

    .content p {
        text-align: center;
        max-width: 280px;
        font-size: 14px;
        line-height: 28px;
        font-weight: 400;
    }


    .content .list li{
        font-size: 14px;
        line-height: 32px;
        justify-content: center;
        font-weight: 500;
        text-align: center;
    }

    .content .list li:not(:last-of-type){
        margin-bottom: 20px;
    }

}



</style>