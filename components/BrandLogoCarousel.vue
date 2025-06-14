<template>
  <div class="bk-brand-area ptb--30">
    <div class="">
      <div class="row">
        <div class="col-lg-12">
          <div class="brand-wrapper">
            <div class="brand__list brand-default brand-style--1">
              <!-- @mouseenter="onPause"
              @mouseleave="onResume" -->
              <swiper
                :slides-per-view="'auto'"
                :space-between="30"
                :speed="5000"
                :loop="true"
                :free-mode="{ enabled: true, sticky: false }"
                :autoplay="swiperOptions.autoplay"
                :breakpoints="swiperOptions.breakpoints"
                class="marquee-swiper"
                @swiper="register"
              >
                <!-- @autoplay-pause="onPause"
                @autoplay-resume="onResume" -->
                <!-- :grab-cursor="false" -->

                <swiper-slide
                  class="brand"
                  v-for="brand in data"
                  :key="brand.id"
                >
                  <nuxt-link to="/">
                    <div class="logo_container">
                      <img :src="brand.logo" alt="logo image" />
                    </div>
                  </nuxt-link>
                </swiper-slide>
              </swiper>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import data from "../data/brandLogo.json";
import SwiperCore from "swiper/core";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay } from "swiper";

SwiperCore.use([Autoplay]);
export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      data,
      savedDuration: "",
      swiperOptions: {
        autoplay: {
          delay: 0, // 每張切換的時間（毫秒）
          disableOnInteraction: false, // 使用者互動後是否停止自動播放（false = 不會停）
          // pauseOnMouseEnter: true,
        },
        breakpoints: {
          1200: {
            slidesPerView: 7,
          },
          768: {
            slidesPerView: 5,
          },
          480: {
            slidesPerView: 3,
          },
        },
      },
    };
  },
  // setup() {
  //   const marqueeSwiper = ref(null);
  //   function register(sw) {
  //     marqueeSwiper.value = sw;
  //     console.log("swiper instance", marqueeSwiper.value);
  //   }
  //   function onPause() {
  //     if (marqueeSwiper.value) {
  //       const currentTranslate = marqueeSwiper.value.getTranslate();
  //       marqueeSwiper.value.setTranslate(currentTranslate);
  //       // marqueeSwiper.value.autoplay.stop();
  //       marqueeSwiper.value.setTransition(0);
  //     }
  //   }
  //   function onResume() {
  //     const sw = marqueeSwiper.value;
  //     if (!sw) return;

  //     sw.setTransition(5000); // 還原 5000ms
  //     sw.slideNext(5000, true); // 推它一格讓畫面動起
  //     sw.autoplay.start(); // 再次啟動計時器
  //   }

  //   return {
  //     register,
  //     onPause,
  //     onResume,
  //   };
  // },
};
</script>

<style lang="scss" scoped>
.marquee-swiper {
  :deep(.swiper-wrapper) {
    transition-timing-function: linear;
  }
}
.bk-brand-area {
  background-color: #faf5eb;
}
.logo_container {
  height: 50px;
  img {
    height: 100%;
  }
}
</style>
