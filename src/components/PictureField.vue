<template>
  <div class="slider-block">
    <swiper :options="swiperOptionTop" class="gallery-top" ref="swiperTop">
      <swiper-slide class="slide-1"></swiper-slide>
      <swiper-slide class="slide-2"></swiper-slide>
      <swiper-slide class="slide-3"></swiper-slide>
      <swiper-slide class="slide-4"></swiper-slide>
      <swiper-slide class="slide-5"></swiper-slide>
      <div class="swiper-button-next swiper-button-white" slot="button-next"></div>
      <div class="swiper-button-prev swiper-button-white" slot="button-prev"></div>
    </swiper>
    <!-- swiper2 Thumbs -->
    <swiper :options="swiperOptionThumbs" class="gallery-thumbs" ref="swiperThumbs">
      <swiper-slide class="slide-1"></swiper-slide>
      <swiper-slide class="slide-2"></swiper-slide>
      <swiper-slide class="slide-3"></swiper-slide>
      <swiper-slide class="slide-4"></swiper-slide>
      <swiper-slide class="slide-5"></swiper-slide>
    </swiper>
  </div>
</template>

<script>
// require styles
import "swiper/dist/css/swiper.css";

import { swiper, swiperSlide } from "vue-awesome-swiper";

export default {
  name: "ProductField",
  components: {
    swiper,
    swiperSlide
  },
  props: {
    msg: String
  },
  data() {
    return {
      swiperOptionTop: {
        spaceBetween: 10,
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev"
        }
      },
      swiperOptionThumbs: {
        spaceBetween: 10,
        centeredSlides: true,
        slidesPerView: "auto",
        touchRatio: 0.2,
        slideToClickedSlide: true
      }
    };
  },
  mounted() {
    this.$nextTick(() => {
      const swiperTop = this.$refs.swiperTop.swiper;
      const swiperThumbs = this.$refs.swiperThumbs.swiper;
      swiperTop.controller.control = swiperThumbs;
      swiperThumbs.controller.control = swiperTop;
    });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
img {
  width: 200px;
  height: auto;
}

.swiper-container {
  background-color: #fff;
}
.slider-block .swiper-slide {
  cursor: pointer;
  background-size: cover;
  background-position: top;
  background-repeat: no-repeat;
  &.slide-1 {
    background-image: url("./../assets/imgs/slide_1.jpeg");
  }
  &.slide-2 {
    background-image: url("./../assets/imgs/slide_2.jpg");
  }
  &.slide-3 {
    background-image: url("./../assets/imgs/slide_3.jpg");
  }
  &.slide-4 {
    background-image: url("./../assets/imgs/slide_4.jpg");
  }
  &.slide-5 {
    background-image: url("./../assets/imgs/slide_5.jpg");
  }
}
.gallery-top {
  height: 80% !important;
  width: 100%;
}
.swiper-container.gallery-top .swiper-slide {
  width: 100% !important;
}
.gallery-thumbs {
  height: 20% !important;
  box-sizing: border-box;
  padding: 10px 0;
}
.gallery-thumbs .swiper-slide {
  width: 25%;
  height: 100%;
  opacity: 0.4;
}
.gallery-thumbs .swiper-slide-active {
  opacity: 1;
}



// @media (max-width: 576px) {
//    html {
//     font-size: 12px;
//   }
//     .container {
//     padding: 0 calc(50vw - 270px);
//     max-width: unset !important;
//     margin: unset !important;
//   }
// }

// @media (min-width: 575.98px){
//   html {
//     font-size: 12px;
//   }
//   .container {
//     padding: 0 calc(50vw - 260px);
//     max-width: unset !important;
//     margin: unset !important;
//   }
// }

// @media (min-width: 767.98px){
//   html {
//     font-size: 14px;
//   }

//   .container {
//     padding: 0 calc(50vw - 370px)!important;
//     max-width: unset !important;
//     margin: unset !important;
//   }
// }

// @media (min-width: 991.98px) {
 
//   .container {
//     padding: 0 calc(50vw - 480px)!important;
//     max-width: unset !important;
//     margin: unset !important;
//   }
// }

</style>
