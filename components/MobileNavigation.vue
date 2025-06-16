<template>
  <div class="mobile-navigation">
    <nav class="offcanvas-navigation" id="offcanvas-navigation">
      <ul>
        <li class="menu-item-has-children">
          <nuxt-link to="/home-masonry-gallery">News & Blog</nuxt-link>
        </li>

        <li
          class="mega--title menu-item-has-children"
          :class="{ active: subMenuIsOpened.aboutUs }"
        >
          <div
            class="nav_item"
            @click="subMenuIsOpened.aboutUs = !subMenuIsOpened.aboutUs"
          >
            About Us
          </div>
          <ul class="sub-menu">
            <li>
              <nuxt-link to="/blog/blog-details"
                ><span>Vision & Mission</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/blog/blog-details"
                ><span>Tainan Local Roots</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/blog/blog-details"
                ><span>Government Partnership</span></nuxt-link
              >
            </li>
          </ul>
        </li>

        <li
          class="mega--title menu-item-has-children"
          :class="{ active: subMenuIsOpened.digitalNomad }"
        >
          <div
            class="nav_item"
            @click="
              subMenuIsOpened.digitalNomad = !subMenuIsOpened.digitalNomad
            "
          >
            Digital Nomads
          </div>
          <ul class="sub-menu">
            <li>
              <nuxt-link to="/blog/blog-details"
                ><span>Tainan Nomad Hub</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/blog/blog-details"
                ><span>Digital Nomad Visa</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/portfolio/portfolio-grid-filter"
                ><span>International Community</span></nuxt-link
              >
            </li>
          </ul>
        </li>

        <li
          class="mega--title menu-item-has-children"
          :class="{ active: subMenuIsOpened.spaces }"
        >
          <div
            class="nav_item"
            @click="subMenuIsOpened.spaces = !subMenuIsOpened.spaces"
          >
            Spaces
          </div>
          <ul class="sub-menu">
            <li>
              <nuxt-link to="/team-grid"
                ><span>Co-working space</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/team-carousel-01"
                ><span>Family & Kids Hub</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/team-carousel-02"
                ><span>Kitchen Commons</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/team-carousel-02"
                ><span>Creative Lab</span></nuxt-link
              >
            </li>
          </ul>
        </li>

        <li
          class="mega--title menu-item-has-children"
          :class="{ active: subMenuIsOpened.trainingCamp }"
        >
          <div
            class="nav_item"
            @click="
              subMenuIsOpened.trainingCamp = !subMenuIsOpened.trainingCamp
            "
          >
            Training Camp
          </div>
          <ul class="sub-menu">
            <li>
              <nuxt-link to="/contact-us-modern"
                ><span>Web Camp</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/contact-us-with-map"
                ><span>Backend camp</span></nuxt-link
              >
            </li>
          </ul>
        </li>

        <li
          class="mega--title menu-item-has-children"
          :class="{ active: subMenuIsOpened.eventsWorkshop }"
        >
          <div
            class="nav_item"
            @click="
              subMenuIsOpened.eventsWorkshop = !subMenuIsOpened.eventsWorkshop
            "
          >
            Events & Workshops
          </div>
          <ul class="sub-menu">
            <li>
              <nuxt-link to="/contact-us-modern"
                ><span>Community Meals</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/contact-us-with-map"
                ><span>Family Workshops</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/contact-us-modern"
                ><span>Creative Lab Programs</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/contact-us-with-map"
                ><span>Sustainability for Everyone</span></nuxt-link
              >
            </li>
          </ul>
        </li>

        <li
          class="mega--title menu-item-has-children"
          :class="{ active: subMenuIsOpened.joinUs }"
        >
          <div
            class="nav_item"
            @click="subMenuIsOpened.joinUs = !subMenuIsOpened.joinUs"
          >
            Join Us
          </div>
          <ul class="sub-menu">
            <li>
              <nuxt-link to="/contact-us-modern"
                ><span>Creators Call</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/contact-us-with-map"
                ><span>Submit Proposal</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/contact-us-modern"
                ><span>Parent Network</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/contact-us-with-map"
                ><span>Partners & Collaborations</span></nuxt-link
              >
            </li>
          </ul>
        </li>

        <li class="menu-item-has-children">
          <nuxt-link to="/home-masonry-gallery">Contact Us</nuxt-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "MobileNavMenu",
  mounted() {
    const offCanvasNav = document.querySelector("#offcanvas-navigation");
    const offCanvasNavSubMenu = offCanvasNav.querySelectorAll(".sub-menu");
    const anchorLinks = offCanvasNav.querySelectorAll("a");

    for (let i = 0; i < offCanvasNavSubMenu.length; i++) {
      offCanvasNavSubMenu[i].insertAdjacentHTML(
        "beforebegin",
        "<span class='menu-expand'><i></i></span>"
      );
    }

    const menuExpand = offCanvasNav.querySelectorAll(".menu-expand");
    const numMenuExpand = menuExpand.length;

    for (let i = 0; i < numMenuExpand; i++) {
      menuExpand[i].addEventListener("click", (e) => {
        sideMenuExpand(e);
      });
    }

    for (let i = 0; i < anchorLinks.length; i++) {
      anchorLinks[i].addEventListener("click", () => {
        closeMobileMenu();
      });
    }

    const sideMenuExpand = (e) => {
      e.currentTarget.parentElement.classList.toggle("active");
    };
    const closeMobileMenu = () => {
      const offcanvasMobileMenu = document.querySelector(
        "#offcanvas-mobile-menu"
      );
      offcanvasMobileMenu?.classList.remove("active");
    };
  },
  setup() {
    const subMenuIsOpened = ref({
      aboutUs: false,
      digitalNomad: false,
      spaces: false,
      trainingCamp: false,
      eventsWorkshop: false,
      joinUs: false,
    });

    return {
      subMenuIsOpened,
    };
  },
};
</script>

<style lang="scss">
.offcanvas-navigation {
  ul {
    li {
      &.menu-item-has-children {
        &.mega--title > {
          a {
            font-weight: 500;
          }
        }
        .sub-menu {
          height: 0;
          opacity: 0;
          transition: 0.3s;
          visibility: hidden;
        }
        &.active > {
          .sub-menu {
            height: 100%;
            opacity: 1;
            visibility: visible;
          }
        }
      }
      a,
      .nav_item {
        color: $white;
        font-size: 14px;
        font-weight: 600;
        padding: 10px 0;
        display: block;
        &:hover {
          color: $theme-color;
          cursor: pointer;
        }
      }
    }
  }

  ul {
    &.sub-menu {
      margin-left: 15px;
      transition: 0.4s;
      li {
        a {
          color: $white;
          font-weight: 400;
          &:hover {
            color: $theme-color;
          }
        }
        .sub-menu {
          li {
            a {
              font-size: 13px;
              padding: 5px 0;
            }
          }
        }
      }
    }
    li {
      &.menu-item-has-children {
        position: relative;
        display: block;
        a {
          display: inline-block;
        }

        &.active > {
          .menu-expand {
            background-color: rgba($white, 0.2);
            i {
              &:before {
                transform: rotate(0);
              }
            }
          }
        }

        .menu-expand {
          top: 5px;
          right: 0;
          width: 35px;
          height: 35px;
          cursor: pointer;
          line-height: 35px;
          position: absolute;
          text-align: center;
          background-color: rgba($white, 0.1);
          &:hover {
            background-color: rgba($white, 0.2);
          }

          i {
            display: block;
            border-bottom: 1px solid #ffffff;
            position: relative;
            width: 10px;
            text-align: center;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            &:before {
              width: 100%;
              content: "";
              border-bottom: 1px solid $white;
              display: block;
              position: absolute;
              top: 0;
              transform: rotate(90deg);
              transition: 0.4s;
            }
          }
        }
      }
    }
  }
}
</style>
