<template>
  <div class="brook-icon-boxes-area plr--100 plr_lg--50 plr_md--50 plr_sm--5">
    <div class="ptb--50 ptb-md--80 ptb-sm--80 bg_color--15">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="brook-section-title text-center mb--20">
              <h6 class="heading heading-h6 theme-color font-blod">About Us</h6>
              <div class="bkseparator--40"></div>
              <h2 class="heading heading-h2 heading-font">
                From Vision to Action
              </h2>
              <h5>Rooted in Tainan, Connected to Community</h5>
            </div>
          </div>
        </div>
        <div class="row mt--30">
          <div
            class="col-lg-3 col-sm-6 mt--40 wow move-up"
            v-for="service in data.services.slice(0, 4)"
            :key="service.id"
          >
            <IconBoxItemOne
              :service="service"
              addClass="bg-transparant plr--50 plr_lg--20 plr_sm--5 plr_md--20"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import data from "../../data/aboutUs.json";

export default {
  components: {
    IconBoxItemOne: () => import("../IconBoxItemOne"),
  },

  data() {
    return {
      data,
    };
  },
};
</script>
