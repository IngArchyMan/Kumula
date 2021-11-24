<template>
  <div class="home">
    <Promotions class="prom-banner"></Promotions>
    <swiper class="home-swiper"
      :modules="modules"
      :slides-per-view="1"
      :space-between="0"
      navigation
      @swiper="onSwiper"
      @slideChange="onSlideChange"
    >
      <swiper-slide>
        <div class="content-slide">
          <div class="bg-slide-overlay"></div>
          <figure>
            <img src="@/assets/img/slide-1.jpg" alt="">
          </figure>
          <h1 class="title-slide">Title Slide</h1>
        </div>
      </swiper-slide>
      <swiper-slide>Slide 2</swiper-slide>
      <swiper-slide>Slide 3</swiper-slide>
    </swiper>
  </div>
</template>

<script>

import Promotions from '@/components/HomeSection/PromotionBanner.vue'
import { Navigation, Pagination, Scrollbar, A11y } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue/swiper-vue';
 import 'swiper/swiper-bundle.css';
export default {
  name: 'Home',
  components: {
    Swiper,
    SwiperSlide,
    Promotions
  },
  setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
        modules: [Navigation, Pagination, Scrollbar, A11y],
      };
    },
}
</script>

<style scoped>
.home{
  width: 100%;
  height: 100vh;
  position: relative;
  overflow: hidden;
}
.prom-banner{
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  max-height: 30px;
  height: 100%;
}
.home-swiper{
  height: 90vh;
  padding: 20px;
  padding-top: 40px;
}
.content-slide{
  display: block;
  width: 100%;
  height: 100%;
  position: relative;
  overflow: hidden;
}
.content-slide .bg-slide-overlay{
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    width: 100%;
    height: 100%;
    background-image: linear-gradient(to left bottom, #ffffff, #e3e3e3, #c8c8c8, #adadad, #939393);
    opacity: 0.35;
    z-index: 11;
}

.content-slide figure{
  width: 100%;
  height: 100%;
  position: relative;
  margin: 0;
  background-color: red;
}
.content-slide figure img{
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.content-slide .title-slide{
  position: absolute;
  right: 10%;
  bottom: 10%;
  z-index: 5;
  color: white;
  font-size: 80px;
}
.home-swiper .swiper-button-next{
  left: 95%;
}
</style>
