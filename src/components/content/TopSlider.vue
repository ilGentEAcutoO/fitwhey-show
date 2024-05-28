<script setup lang="ts">
import { Swiper, SwiperSlide } from 'swiper/vue';
import {IonImg} from "@ionic/vue";

import { Navigation, Pagination, Scrollbar, A11y } from 'swiper/modules';
import { ref } from 'vue';
import 'swiper/css';
import 'swiper/css/autoplay';
import 'swiper/css/keyboard';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';
import 'swiper/css/zoom';

const slideNumber = ref(1);
const modules = [Navigation, Pagination, Scrollbar, A11y];

function slideChange($event: any) {
  slideNumber.value = $event.activeIndex + 1;
}


</script>

<template>
  <div class="slider-item pd-image-slider">
    <!--          <ion-buttons class="slide-btn-left">-->
    <!--            <img src="/assets/icon/swipe-arrow-left.svg">-->
    <!--          </ion-buttons>-->
    <!--          <ion-buttons class="slide-btn-right">-->
    <!--            <img src="/assets/icon/swipe-arrow-right.svg">-->
    <!--          </ion-buttons>-->
    <div class="product-label">
      <span>5lb</span>
    </div>
    <div class="slide-count">
      <span>{{slideNumber}}/3</span>
    </div>
    <swiper class="swiper-wrapper pd-image-slide"
            navigation
            :modules="modules"
            @slideChange="slideChange">
      <swiper-slide class="swiper-slide">
        <ion-img src="/assets/img/place-holder0.png" class="slides-product-image"></ion-img>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <ion-img src="/assets/img/place-holder0-1.png" class="slides-product-image"></ion-img>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <ion-img src="/assets/img/place-holder3.png" class="slides-product-image"></ion-img>
      </swiper-slide>
    </swiper>

    <div class="tier-level">
      <span class="sub-text">Your Tier</span>
      <span class="main-text">
                            <img src="/assets/icon/dumbbell-icon.svg">
                          Pro Member
                        </span>
    </div>
  </div>

</template>

<style scoped>

</style>