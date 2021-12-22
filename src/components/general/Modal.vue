<template>
  <transition name="fade">
    <div class="modal" v-if="show">
      <div class="modal__backdrop" @click="closeModal()"/>
      <div class="modal__dialog">
        <div class="modal__header">
          <slot name="header"/>
           <svg width="57" height="57" viewBox="0 0 57 57" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect width="57" height="57" rx="28.5" fill="#311747"/>
                <g clip-path="url(#clip0_1460_2672)">
                <path d="M32.9281 36.8301L34.6601 37.8301L33.6601 39.5622L16.3396 29.5622L17.3396 27.8301L19.0717 28.8301L22.5717 22.768C23.6325 20.9305 25.3799 19.5897 27.4293 19.0405C29.4787 18.4914 31.6624 18.7789 33.4999 19.8398C35.3373 20.9006 36.6781 22.648 37.2273 24.6974C37.7764 26.7468 37.4889 28.9305 36.4281 30.768L32.9281 36.8301ZM21.4018 34.7942L26.5979 37.7942L25.5979 39.5263L20.4018 36.5263L21.4018 34.7942Z" fill="white"/>
                </g>
                <defs>
                <clipPath id="clip0_1460_2672">
                <rect width="24" height="24" fill="white" transform="translate(24.1077 12.1077) rotate(30)"/>
                </clipPath>
                </defs>
            </svg>
        </div>

        <div class="modal__body">
          <slot name="body"/>
          <h3>
              Get Notified
          </h3>
          <p>
              We are still in active development of ChurchRUSH. We love to keep you updated about what we are donig and when we go live. Please choose the category you fall into to below.
          </p>
        </div>

        <div class="modal__footer">
          <slot name="footer"/>
          <button class="ind" @click="closeModal()">
              Individual
          </button>
          <button class="chu" @click="closeModal()">
              Church
          </button>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: "Modal",
  data() {
    return {
      show: false
    };
  },
  methods: {
    closeModal() {
      this.show = false;
      document.querySelector("body").classList.remove("overflow-hidden");
    },
    openModal() {
      this.show = true;
      document.querySelector("body").classList.add("overflow-hidden");
    }
  }
};
</script>


<style lang="css" scoped>

.modal {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 999999999;
  overflow-x: hidden;
  overflow-y: auto;
  display: grid;
  place-items: center;
}

.modal .modal__backdrop {
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: rgba(0, 0, 0, 0.3);
    z-index: 9;
}

.modal .modal__dialog {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 32px 72px;
    position: relative;
    width: 517px;
    height: 357px;
    background: #FFFFFF;
    border-radius: 32px;
    z-index: 999;
}

.modal__dialog .modal__header {
    width: 100%;
    height: fit-content;
    display: grid;
    place-items: center;
    margin-bottom: 32px;
}

.modal__dialog .modal__body {
    width: 100%;
    height: fit-content;
    display: grid;
    place-items: center;
    margin-bottom: 32px;
}
.modal__dialog .modal__body h3 {
    font-weight: 600;
    font-size: 24px;
    line-height: 20px;
    text-align: center;
    color: #000000;
}
.modal__dialog .modal__body p {
    font-style: normal;
    font-weight: 300;
    font-size: 14px;
    line-height: 20px;
    text-align: center;
    color: #080C10;
    max-width: 373px;
    /* margin: 24px 0px; */
}

.modal__dialog  .modal__footer {
    width: 100%;
    height: fit-content;
    display: flex;
    align-items: center;
    justify-content: center;
}
.modal__dialog  .modal__footer .ind {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 8px 40px;
    text-align: center;
    letter-spacing: -0.3px;
    color: #FAFAFA;
    position: static;
    width: 126px;
    height: 48px;
    left: 0px;
    top: 0px;
    background: #311747;
    border-radius: 12px;
    font-family: 'Poppins', sans-serif;
    font-style: normal;
    font-weight: normal;
    font-size: 14px;
    outline: 0;
    border: 0;
    margin: 0px 32px;
    cursor: pointer;
}
.modal__dialog  .modal__footer .chu {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 8px 40px;
    text-align: center;
    letter-spacing: -0.3px;
    color: #311747;
    position: static;
    width: 126px;
    height: 48px;
    left: 0px;
    top: 0px;
    border: 1px solid #311747;
    border-radius: 12px;
    font-family: 'Poppins', sans-serif;
    font-style: normal;
    font-weight: normal;
    font-size: 14px;
    outline: 0;
    margin: 0px 32px;
    cursor: pointer;
    background: transparent;
}

 .fade-enter-active,
 .fade-leave-active {
   transition: opacity 0.2s;
 }
 .fade-enter,
 .fade-leave-to {
   opacity: 0;
 } 



/* Responsiveness */

/* 600px */

@media (max-width:600px) {

    .modal .modal__dialog {
      padding: 32px 35px;
      max-width: 320px;
      min-height: 450px;
    }


    .modal__dialog  .modal__footer {
        flex-wrap: wrap;
    }

    .modal__dialog  .modal__footer button {
      display: block;
    }

    .modal__dialog  .modal__footer .ind {
      margin-bottom: 16px;
    }

}


/* 

//   &__close {
//     width: 30px;
//     height: 30px;
//   }
//   &__header {
//     display: flex;
//     align-items: flex-start;
//     justify-content: space-between;
//     padding: 20px 20px 10px;
//   }
//   &__body {
//     padding: 10px 20px 10px;
//     overflow: auto;
//     display: flex;
//     flex-direction: column;
//     align-items: stretch;
//   }
//   &__footer {
//     padding: 10px 20px 20px;
//   }
// }
// .fade-enter-active,
// .fade-leave-active {
//   transition: opacity 0.2s;
// }
// .fade-enter,
// .fade-leave-to {
//   opacity: 0;
// } */
</style>
