<template>
  <nav class="page_nav">
    <ul class="mainmenu">
      <li class="lavel-1 slide--megamenu">
        <nuxt-link to="/home-masonry-gallery">
          <span>News & Blog</span>
        </nuxt-link>
      </li>

      <li class="lavel-1 with--drop slide--megamenu">
        <nuxt-link to="/portfolio/portfolio-grid-boxed">
          <span>About</span>
        </nuxt-link>
        <ul class="mega__width--fullscreen">
          <div class="container">
            <div class="mega__list">
              <li class="mega--title">
                About Us
                <ul>
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
              <li class="mega--title">
                Digital Nomads
                <ul>
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
              <li class="mega--title">
                Spaces
                <ul>
                  <li>
                    <nuxt-link to="/portfolio/portfolio-details"
                      ><span>Co-working space</span></nuxt-link
                    >
                  </li>

                  <li>
                    <nuxt-link to="/portfolio/portfolio-details"
                      ><span>Family & Kids Hub</span></nuxt-link
                    >
                  </li>
                  <li>
                    <nuxt-link to="/portfolio/portfolio-details"
                      ><span>Kitchen Commons</span></nuxt-link
                    >
                  </li>
                  <li>
                    <nuxt-link to="/portfolio/portfolio-details"
                      ><span> Creative Lab</span></nuxt-link
                    >
                  </li>
                </ul>
              </li>
            </div>
          </div>
        </ul>
      </li>

      <li class="lavel-1 with--drop slide--megamenu">
        <nuxt-link to="">
          <span>Work</span>
        </nuxt-link>
        <ul class="mega__width--fullscreen">
          <div class="container">
            <div class="mega__list">
              <li class="mega--title">
                Code
                <ul>
                  <li>
                    <nuxt-link to="/blog/blog-grid-mesonry"
                      ><span>Web Camp</span></nuxt-link
                    >
                  </li>
                  <li>
                    <nuxt-link to="/blog/blog-grid-mesonry"
                      ><span>Backend camp</span></nuxt-link
                    >
                  </li>
                </ul>
              </li>
              <li class="mega--title">
                Creativity
                <ul>
                  <li>
                    <nuxt-link to="/portfolio/portfolio-grid-filter"
                      ><span>SDGs & UN 2.0 School</span></nuxt-link
                    >
                  </li>
                  <li>
                    <nuxt-link to="/portfolio/portfolio-grid-filter"
                      ><span>Future Food Studio</span></nuxt-link
                    >
                  </li>
                  <li>
                    <nuxt-link to="/portfolio/portfolio-grid-filter"
                      ><span>Worldschooling</span></nuxt-link
                    >
                  </li>
                  <li>
                    <nuxt-link to="/portfolio/portfolio-grid-filter"
                      ><span>Creative Lab Programs</span></nuxt-link
                    >
                  </li>
                  <li>
                    <nuxt-link to="/portfolio/portfolio-grid-filter"
                      ><span>Sustainability for Everyone</span></nuxt-link
                    >
                  </li>
                </ul>
              </li>
              <li class="mega--title">
                Life
                <ul>
                  <li>
                    <nuxt-link to="/portfolio/portfolio-grid-filter"
                      ><span>Community Meals</span></nuxt-link
                    >
                  </li>
                  <li>
                    <nuxt-link to="/portfolio/portfolio-grid-filter"
                      ><span> Family Workshops</span></nuxt-link
                    >
                  </li>
                </ul>
              </li>
            </div>
          </div>
        </ul>
      </li>

      <li class="lavel-1 with--drop slide--megamenu">
        <nuxt-link to="/blog/blog-creative">
          <span>Contact</span>
        </nuxt-link>
        <ul class="mega__width--fullscreen">
          <div class="container">
            <div class="mega__list">
              <li class="mega--title">
                Join Us
                <ul>
                  <li>
                    <nuxt-link to="/blog/blog-creative"
                      ><span>Creators Call</span></nuxt-link
                    >
                  </li>
                  <li>
                    <nuxt-link to="/blog/blog-standard-list"
                      ><span>Submit Proposal</span></nuxt-link
                    >
                  </li>
                  <li>
                    <nuxt-link to="/blog/blog-grid-classic"
                      ><span>Parent Network</span></nuxt-link
                    >
                  </li>
                  <li>
                    <nuxt-link to="/blog/blog-grid-classic"
                      ><span>Partners & Collaborations</span></nuxt-link
                    >
                  </li>
                </ul>
              </li>
              <li class="mega--title">
                Stay in Touch
                <ul>
                  <li>
                    <nuxt-link to="/blog/blog-grid-classic-sidebar"
                      ><span>Contact Info</span></nuxt-link
                    >
                  </li>
                </ul>
              </li>
            </div>
          </div>
        </ul>
      </li>
    </ul>
  </nav>
</template>

<style lang="scss">
.mega__list {
  display: flex;
  li {
    flex-basis: 25%;
  }
}
</style>
