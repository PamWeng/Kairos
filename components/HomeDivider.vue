<template>
  <div>
    <div
      class="brook-call-to-action bg_image--9 ptb--50"
      :style="{
        backgroundImage: `url(${useAssetUrl(`img/goodIdea/${props.img}`)})`,
      }"
    >
      <div class="container">
        <div class="row align-items-center">
          <div class="col-lg-12 col-sm-12 col-12">
            <div class="call-content text-center text-sm-start">
              <!-- <h3 class="heading heading-h3 text-white wow move-up">
                {{ props.title }}
              </h3> -->
              <div class="text-center">
                <h6 class="heading font-blod theme-color">
                  {{ props.text.title }}
                </h6>
                <div class="bkseparator--40"></div>
                <h2 class="heading heading-font text-white">
                  {{ props.text.content }}
                </h2>
              </div>
            </div>
          </div>
          <!-- <div class="col-lg-6 col-sm-6 col-12">
            <div
              class="call-btn text-center text-sm-right mt_mobile--20 wow move-up"
            >
              <nuxt-link
                to="/contact-us-modern"
                class="brook-btn bk-btn-theme btn-sd-size btn-rounded"
                >Find out more</nuxt-link
              >
            </div>
          </div> -->
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  text: {
    type: Object,
    default: () => ({
      title: "",
      content: "",
    }),
  },
  img: {
    type: String,
    default: "",
  },
});
</script>

<style lang="scss" scoped></style>
