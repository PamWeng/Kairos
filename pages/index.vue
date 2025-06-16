<template>
  <div class="main-container">
    <!-- <HeaderOnepageMirror
      @toggleFullpageMenu="fullpageOpen = !fullpageOpen"
      @togglenav="navOpen = !navOpen"
    /> -->
    <HeaderBlack
      @togglenav="navOpen = !navOpen"
      @toggleSearch="searchOpen = !searchOpen"
    />
    <OffcanvasMenu
      :class="{ 'is-visiable': fullpageOpen }"
      @toggleFullpageMenu="fullpageOpen = !fullpageOpen"
    />
    <OffCanvasMobileMenu
      :class="{ 'show-mobile-menu': navOpen }"
      @togglenav="navOpen = !navOpen"
    />
    <!-- <HeroOnepage /> -->

    <!--insert banner -->
    <HeroAuthenticStudio />
    <!--insert banner end -->
    <div
      class="brook-call-to-action bg_image--33 ptb--40 ptb-md--80 ptb-sm--80"
    >
      <!-- :style="{ backgroundColor: '#CDBB69' }" -->
      <!-- :style="{ backgroundImage: `url('/img/bg/bg-image-33.jpg')` }" -->
      <!-- divider -->
      <div class="container">
        <div class="row align-items-center">
          <div class="col-12">
            <div class="call-content text-center">
              <h3 class="heading heading-h3 theme-color">
                Updates & Stories
                <!-- <span class="tarkis-color">Create a project</span> -->
              </h3>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- divider end -->

    <!-- updates -->
    <div class="bk-blog-grid-area ptb--50 ptb-md--80 ptb-sm--80 bg_color--10">
      <div class="container">
        <div class="row gy-4">
          <div
            class="col-lg-4 col-sm-6 move-up wow"
            v-for="blog in data.blogs.slice(6, 9)"
            :key="blog.id"
          >
            <BlogPostThree :blog="blog" addClass="grid-simple" />
          </div>
        </div>
      </div>
    </div>
    <!-- updates end -->

    <!-- <CurveShape>
      <template v-slot:bgcolor>
        <path
          style="fill: #f4efff; stroke-miterlimit: 10"
          d="M3360.5,97.739c-242,0-480-48.375-480-48.375
                        S2647.5,0.5,2400.5,0.5s-480,48.375-480,48.375s-238,48.864-480,48.864s-480-48.375-480-48.375S727.5,0.5,480.5,0.5
                        S0.5,48.875,0.5,48.875V108h1920h1920V48.875C3840.5,48.875,3602.5,97.739,3360.5,97.739z"
        />
      </template>
    </CurveShape> -->
    <!-- <MusicianIconBox /> -->
    <!-- divider -->
    <HomeDivider
      :text="{ title: 'what we do', content: 'Updates, Roots, Impact' }"
      :img="'IMG_5939.jpg'"
    />
    <!-- divider end-->
    <!-- what we do section -->
    <div class="row row--30 pl--30 pr--30 pb--60 bg_color--5">
      <div
        class="col-xl-4 col-sm-6 col-12 move-up wow mt--60"
        v-for="blog in data.blogs.slice(0, 6)"
        :key="blog.id"
      >
        <div
          class="blog-grid-minimal"
          :style="{
            backgroundColor: `${blog.bgColor}`,
          }"
        >
          <div
            class="grid-overlay"
            :style="{
              backgroundImage: `url(${useAssetUrl(blog.image)})`,
            }"
          ></div>
          <div class="post-content">
            <div class="post-meta">
              <div class="post-date">{{ blog.date }}</div>
              <!-- <div class="post-category">
                <nuxt-link
                  v-for="(category, i) in blog.categories.slice(0, 1)"
                  :key="i"
                  :to="`/blog/category/${slugify(category)}`"
                  >{{ category }}</nuxt-link
                >
              </div> -->
            </div>
            <h5 class="heading">
              <nuxt-link :to="`/blog/${blog.slug}`">
                {{ blog.title }}
              </nuxt-link>
            </h5>
          </div>
        </div>
      </div>
    </div>
    <!-- what we do section end -->

    <!-- divider -->
    <div class="row">
      <div class="col-lg-12">
        <div class="text-center mb--50 mt--50">
          <h6 class="heading font-blod theme-color">Space</h6>
          <div class="bkseparator--40"></div>
          <h2 class="heading heading-font">
            Made for Sharing — Ideas, Care and Food
          </h2>
        </div>
      </div>
    </div>
    <!-- divider end-->
    <MusicianPortfolioGallery :img-list="whatWeDoImgList" />
    <!-- <OnepageTeammember /> -->
    <!-- <TestimonialSix /> -->

    <!-- <MusicianCounterup /> -->

    <ServiceIconBoxWithTitleStyleTwo class="pt-0 pb-0 mt--50 mb--50" />
    <BrandLogoCarousel />

    <div
      class="bg_image--34 ptb--130 ptb-md--80 ptb-sm--80"
      :style="{
        backgroundImage: `url(${useAssetUrl('/img/goodIdea/IMG_5939.jpg')})`,
      }"
    >
      <div class="container">
        <div class="row align-items-center">
          <div class="col-lg-4 col-md-12 col-12">
            <div class="on-page-call-content">
              <div class="call-content text-center text-sm-start">
                <h2 class="heading heading-h2 text-white">
                  Start a new <br />
                  project ?
                </h2>
              </div>
              <div class="call-btn mt--60 mt_md--40 mt_sm--40">
                <nuxt-link
                  to="/contact-us-modern"
                  class="brook-btn bk-btn-white text-theme btn-sd-size btn-rounded"
                  >Contact now</nuxt-link
                >
              </div>
            </div>
          </div>
          <div class="col-lg-8 col-md-12 col-12 mt_md--40 mt_sm--40">
            <div class="onepage-contact-inner bg_color--1">
              <div class="page-address-inner">
                <!-- Start Single Address -->
                <div class="address-content">
                  <h5 class="heading heading-h5 font-20">
                    Visit our studio at
                  </h5>
                  <div class="address mt--10">
                    <p class="bk_pra font-16 line-height-1-87">
                      2005 Stokes Isle Apt. 896, <br />
                      Vacaville 10010, USA
                    </p>
                  </div>
                </div>

                <!-- Start Single Address -->
                <div class="address-content bk-hover mt--50 mt_lg--20">
                  <h5 class="heading heading-h5 font-20">Message us</h5>
                  <div class="address mt--10">
                    <p class="bk_pra font-16 line-height-1-87">
                      <a class="color-dark" href="mailto:info@yourdomain.com"
                        >info@yourdomain.com</a
                      >
                    </p>
                    <p class="bk_pra font-16 line-height-1-87">
                      <a class="color-dark" href="tel:(+68)120034509"
                        >(+68) 120034509</a
                      >
                    </p>
                  </div>
                </div>

                <!-- Start Single Address -->
                <div class="address-content mt--50 mt_lg--20">
                  <div class="social-share social--transparent">
                    <a href="https://www.facebook.com/" target="_blank">
                      <i class="fab fa-facebook"></i>
                    </a>
                    <a href="https://twitter.com/" target="_blank">
                      <i class="fab fa-twitter"></i>
                    </a>
                    <a href="https://www.instagram.com/" target="_blank">
                      <i class="fab fa-instagram"></i>
                    </a>
                    <a href="https://dribbble.com/" target="_blank">
                      <i class="fab fa-dribbble"></i>
                    </a>
                    <a href="https://www.pinterest.com/" target="_blank">
                      <i class="fab fa-pinterest"></i>
                    </a>
                  </div>
                </div>
              </div>
              <div class="googlemap">
                <GoogleMap />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <FooterTwo />
  </div>
</template>

<script>
import data from "~/data/whatWeDo.json";
import SwiperCore, { Navigation } from "swiper/core";
import { Swiper, SwiperSlide } from "swiper/vue";
import ServiceIconBoxWithTitleStyleTwo from "@/components/sections/ServiceIconBoxWithTitleStyleTwo";

SwiperCore.use([Navigation]);

export default {
  components: {
    HeaderOnepageMirror: () => import("@/components/HeaderOnepageMirror"),
    OffcanvasMenu: () => import("@/components/OffcanvasMenu"),
    OffCanvasMobileMenu: () => import("@/components/OffCanvasMobileMenu"),
    HeroOnepage: () => import("@/components/HeroOnepage"),
    MusicianIconBox: () => import("@/components/MusicianIconBox"),
    MusicianPortfolioGallery: () =>
      import("@/components/MusicianPortfolioGallery"),
    OnepageTeammember: () => import("@/components/OnepageTeammember"),
    TestimonialSix: () => import("@/components/TestimonialSix"),
    MusicianCounterup: () => import("@/components/MusicianCounterup"),
    BlogPostThree: () => import("@/components/BlogPostThree"),
    BrandLogoCarousel: () => import("@/components/BrandLogoCarousel"),
    GoogleMap: () => import("@/components/GoogleMap"),
    FooterTwo: () => import("@/components/FooterTwo"),
    CurveShape: () => import("@/components/CurveShape"),
    Swiper,
    SwiperSlide,
    ServiceIconBoxWithTitleStyleTwo,
  },

  data() {
    return {
      data,
      fullpageOpen: false,
      navOpen: false,
      swiperOptions: {
        navigation: {
          nextEl: ".ht-swiper-button-next",
          prevEl: ".ht-swiper-button-prev",
        },
        breakpoints: {
          768: {
            slidesPerView: 2,
          },
          320: {
            centeredSlides: false,
            slidesPerView: 1,
          },
        },
      },
      whatWeDoImgList: [
        {
          url: useAssetUrl("img/goodIdea/img_21.png"),
          text: "UIJ-market-at-night",
        },
        {
          url: useAssetUrl("img/goodIdea/S__325255199_0.jpg"),
          text: "little-village-xmas",
        },
        {
          url: useAssetUrl("img/goodIdea/S__325255198_0.jpg"),
          text: "make-cookies",
        },
        {
          url: useAssetUrl("img/goodIdea/IMG_7610.jpg"),
          text: "future-factory",
        },
      ],
    };
  },
  mounted() {
    document.body.classList.add("template-color-10", "template-font-3");
  },
  unmounted() {
    document.body.classList.remove("template-color-10", "template-font-3");
  },
};
</script>
<style lang="scss" scoped>
.hero-blog-grid-item {
  height: 600px;
  display: flex;
  align-items: center;
  justify-content: center;
  // res
  @media #{$sm-layout} {
    height: 400px;
  }
}
.hero-blog-grid-content {
  .post-inner {
    padding-top: 250px;
    @media #{$sm-layout} {
      padding-top: 150px;
    }
    .heading {
      font-size: 36px;
      margin-bottom: 20px;
      // res
      @media #{$md-layout, $sm-layout} {
        font-size: 24px;
      }
      a {
        color: $white;
        &:hover {
          color: $color-18;
        }
      }
    }
    .post-meta {
      color: $white;
      .post-date {
        color: $white;
      }
      .post-category {
        a {
          color: $white;
          &:hover {
            color: $color-18;
          }
        }
      }
    }
  }
}
//custom
.post-content {
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
}
</style>
