<template>
  <div class="brook-hero-number-slider-area position-relative">
    <div class="brook-element-carousel number-dot">
      <swiper
        :speed="1000"
        :loop="false"
        :pagination="swiperOptions.pagination"
        :effect="'fade'"
        :autoplay="swiperOptions.autoplay"
      >
        <swiper-slide v-for="slide in sliders" :key="slide.id">
          <nuxt-link to="/about-us-01">
            <div
              class="hero-item bg-image"
              :style="{ backgroundImage: `url(${slide.bgImage})` }"
            >
              <div class="container">
                <div class="hero-content-2">
                  <h6>{{ slide.subHeading }}</h6>
                  <h3>{{ slide.heading }}</h3>
                </div>
              </div>
            </div>
          </nuxt-link>
        </swiper-slide>
      </swiper>
      <!-- Add Pagination -->
      <div class="swiper-pagination"></div>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import SwiperCore, { Pagination, EffectFade } from "swiper/core";
import { Autoplay } from "swiper";
SwiperCore.use([Pagination, EffectFade]);
SwiperCore.use([Autoplay]);

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      swiperOptions: {
        autoplay: {
          delay: 5000, // 每張切換的時間（毫秒）
          disableOnInteraction: false, // 使用者互動後是否停止自動播放（false = 不會停）
        },
        pagination: {
          el: ".swiper-pagination",
          clickable: true,
          renderBullet: function (index, className) {
            return '<span class="' + className + '">' + (index + 1) + "</span>";
          },
        },
      },

      sliders: [
        {
          id: 1,
          heading: "revolutionary creations and exquisite designs.",
          subHeading: "WE WORK SMART, WE PLAY HARD",
          bgImage: useAssetUrl("img/goodIdea/UI-market-with-sprout.png"),
        },
        {
          id: 2,
          heading: "revolutionary creations and exquisite designs.",
          subHeading: "WE WORK SMART, WE PLAY HARD",
          bgImage: useAssetUrl("img/goodIdea/DSC00230.jpg"),
        },
        {
          id: 3,
          heading: "revolutionary creations and exquisite designs.",
          subHeading: "WE WORK SMART, WE PLAY HARD",
          bgImage: useAssetUrl("img/goodIdea/20250412-3.jpg"),
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.container {
  margin-top: auto;
}
.hero-content-2 {
  h3,
  h6 {
    text-align: right;
    margin-bottom: 0px;
  }
  h3 {
    font-size: 38px;
  }
}
.hero-item {
  padding: 120px 80px;
}
</style>
