<template>
  <div class="bk-portfolio-area">
    <div class="portfolio-wrapper">
      <div class="row row--0">
        <div class="col-lg-12 col-xl-6">
          <div class="portfolio-cation wow move-up">
            <div class="thumb">
              <img
                :src="
                  props?.imgList[0].url ||
                  `/img/portfolio/portfolio-1/portfolio-1.jpg`
                "
                :alt="props?.imgList[0].text || `Portfolio Images`"
                style="aspect-ratio: 1/1; object-fit: cover"
              />
            </div>
            <div class="port-overlay-info">
              <div class="hover-action">
                <h3 class="post-overlay-title">
                  <nuxt-link to="/portfolio/portfolio-details"
                    >A Golden Age of Design</nuxt-link
                  >
                </h3>
                <div class="category">Design</div>
              </div>
            </div>
          </div>
        </div>

        <div class="col-lg-12 col-xl-6">
          <div class="row row--0">
            <div class="col-lg-12">
              <!-- Start Single Portfolio -->
              <div class="portfolio-cation wow move-up">
                <div class="thumb">
                  <img
                    :src="
                      props?.imgList[1].url ||
                      `/img/portfolio/portfolio-1/portfolio-2.jpg`
                    "
                    :alt="props?.imgList[1].text || `Portfolio Images`"
                    style="aspect-ratio: 2/1; object-fit: cover"
                  />
                </div>
                <div class="port-overlay-info">
                  <div class="hover-action">
                    <h3 class="post-overlay-title">
                      <nuxt-link to="/portfolio/portfolio-details"
                        >Web Comic Landscape</nuxt-link
                      >
                    </h3>
                    <div class="category">Design</div>
                  </div>
                </div>
              </div>
              <!-- End Single Portfolio -->
            </div>
            <div class="col-lg-6">
              <!-- Start Single Portfolio -->
              <div class="portfolio-cation wow move-up">
                <div class="thumb">
                  <img
                    :src="
                      props?.imgList[2].url ||
                      `/img/portfolio/portfolio-1/portfolio-3.jpg`
                    "
                    :alt="props?.imgList[2].text || `Portfolio Images`"
                    style="aspect-ratio: 1/1; object-fit: cover"
                  />
                </div>
                <div class="port-overlay-info">
                  <div class="hover-action">
                    <h3 class="post-overlay-title">
                      <nuxt-link to="/portfolio/portfolio-details"
                        >Website Success Prospects</nuxt-link
                      >
                    </h3>
                    <div class="category">Marketing</div>
                  </div>
                </div>
              </div>
              <!-- End Single Portfolio -->
            </div>
            <div class="col-lg-6">
              <!-- Start Single Portfolio -->
              <div class="portfolio-cation wow move-up">
                <div class="thumb">
                  <img
                    :src="
                      props?.imgList[3].url ||
                      `/img/portfolio/portfolio-1/portfolio-4.jpg`
                    "
                    :alt="props?.imgList[3].text || `Portfolio Images`"
                    style="aspect-ratio: 1/1; object-fit: cover"
                  />
                </div>
                <div class="port-overlay-info">
                  <div class="hover-action">
                    <h3 class="post-overlay-title">
                      <nuxt-link to="/portfolio/portfolio-details"
                        >New Age Design</nuxt-link
                      >
                    </h3>
                    <div class="category">Life Style</div>
                  </div>
                </div>
              </div>
              <!-- End Single Portfolio -->
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
const props = defineProps({
  imgList: {
    type: Array,
    default: () => [],
  },
});
</script>
<style scoped>
.fill_container {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
