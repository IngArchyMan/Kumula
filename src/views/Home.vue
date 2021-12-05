<template>
  <div class="home">
    <Promotions class="prom-banner"></Promotions>
    <swiper class="home-swiper"
      :modules="modules"
      :slides-per-view="1"
      :space-between="10"
      :navigation="true"
      :loop="true"
      autoplay
      @swiper="onSwiper"
      @slideChange="onSlideChange"
    >
      <swiper-slide v-slot="{ isActive }">
        <div class="content-slide">
          <div class="bg-slide-overlay"></div>
          <figure>
            <img src="@/assets/img/slide-1.jpg" alt="">
          </figure>
          <h1 class="title-slide" :class="{'appear': isActive}">Title Slide</h1>
        </div>
      </swiper-slide>
      <swiper-slide v-slot="{ isActive }" data-swiper-autoplay="2000">
        <div class="content-slide">
          <div class="bg-slide-overlay"></div>
          <figure>
            <img src="@/assets/img/slide-2.jpg" alt="">
          </figure>
          <h1 class="title-slide" :class="{'appear': isActive}">Title Slide</h1>
        </div>
      </swiper-slide>
      <swiper-slide v-slot="{ isActive }">
        <div class="content-slide">
          <div class="bg-slide-overlay"></div>
          <figure>
            <img src="@/assets/img/slide-3.jpg" alt="">
          </figure>
          <h1 class="title-slide" :class="{'appear': isActive}">Title Slide</h1>
        </div>
      </swiper-slide>
      <swiper-slide v-slot="{ isActive }">
        <div class="content-slide">
          <div class="bg-slide-overlay"></div>
          <figure>
            <img src="@/assets/img/slide-4.jpg" alt="">
          </figure>
          <h1 class="title-slide" :class="{'appear': isActive}">Title Slide</h1>
        </div>
      </swiper-slide>
    </swiper>
    <About></About>
    <Services></Services>
  </div>
</template>

<script>

import Promotions from '@/components/Home/PromotionBanner.vue'
import About from '@/components/Home/AboutSection.vue'
import Services from '@/components/Home/ServicesSection.vue'
import { Navigation, A11y, Autoplay } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue/swiper-vue';
import 'swiper/swiper-bundle.css';
export default {
  name: 'Home',
  components: {
    Swiper,
    SwiperSlide,
    Promotions,
    About,
    Services
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
        modules: [Navigation, A11y, Autoplay],
      };
    },
}
</script>

<style>

.home{
  width: 100%;
  height: 100vh;
  max-width: 100vw;
  position: relative;
  overflow-x: hidden;
  margin: 0;padding: 0;
}
.prom-banner{
  max-height: 40px;
  height: 100%;
  background-color: #574A61;
  color: white;
}
.home-swiper{
  width: 100%;
  height: 100%;
}
.home .swiper .swiper-wrapper .swiper-slide{
  display: flex;
  justify-content: center;
  align-items: center;
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
    width: 99%;
    height: 98%;
    background-image: linear-gradient(to left bottom, #ffffff, #e3e3e3, #c8c8c8, #adadad, #939393);
    opacity: 0.35;
    z-index: 11;
    margin: auto;
}

.content-slide figure{
  width: 100%;
  height: 100%;
  position: relative;
  margin: 0;
}
.content-slide figure img{
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  width: 100%;
  height: 100%;
  padding: 10px;
  margin: auto;
  object-fit: cover;
}
.content-slide .title-slide{
  margin: 0;
  position: absolute;
  right: 10%;
  bottom: 10%;
  z-index: 5;
  color: white;
  font-size: 130px;
  transform: translateY(-100%);
  opacity: 0;
  transition: 1s all ease-in-out;
  text-decoration: underline;
}
.content-slide .title-slide.appear{
  transform: translateY(0%);
  opacity: 1;
}

.home .swiper .swiper-button-next, .home .swiper .swiper-button-prev{
  width: 42px;
  height: 68px;
  background-color: #795548;
  color: white;
  transform: skewX(10deg);
  top: 85%;
}
.home .swiper .swiper-button-next{
  left: 5%;
}
.home .swiper .swiper-button-prev{
  left: 3%;
}
.home .swiper .swiper-button-next::after, .home .swiper .swiper-button-prev::after{
  font-size: 32px;
}
.home .swiper .swiper-button-next.swiper-button-disabled, .home .swiper .swiper-button-prev.swiper-button-disabled{
  height: 52px;
  top: 91.7%;
}

@media only screen and (max-width: 576px) {
  .home .swiper .swiper-button-next, .home .swiper .swiper-button-prev{
    top: 90%;
  }
  .home .swiper .swiper-button-next{
    left: 20%;
  }
  .home .swiper .swiper-button-prev{
    left: 10%;
  }
  .home .swiper .swiper-button-next.swiper-button-disabled, .home .swiper .swiper-button-prev.swiper-button-disabled{
    top: 92%;
  }
  .home-swiper{
    height: 90vh;
  }
  .content-slide .title-slide{
    right: 8%;
    transform: translateX(50%);
    font-size: 75px;
    bottom: 20%;
  }
}
</style>
