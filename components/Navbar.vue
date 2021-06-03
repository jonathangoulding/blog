<template>
  <nav class="navbar" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <!--        <a class="navbar-item" href="https://bulma.io">-->
      <!--          <img src="/images/public_img_backgrounds_grass-green-plants-natural.jpg" width="50" height="28">-->
      <!--        </a>-->

      <a
        role="button"
        class="navbar-burger"
        aria-label="menu"
        data-target="navbarBasicExample"
        :aria-expanded="isActive"
        :class="{ 'is-active': isActive }"
        @click="isActive = !isActive"
      >
        <span aria-hidden="true" />
        <span aria-hidden="true" />
        <span aria-hidden="true" />
      </a>
    </div>

    <div id="collapse" :class="{ 'is-active': isActive }" class="navbar-menu">
      <div class="navbar-start">
        <nuxt-link to="/" class="navbar-item">
          Home
        </nuxt-link>

        <nuxt-link to="/blog" class="navbar-item">
          Blog
        </nuxt-link>

        <div class="navbar-item has-dropdown is-hoverable">
          <a class="navbar-link">
            More
          </a>

          <div class="navbar-dropdown">
            <a class="navbar-item">
              About
            </a>
            <a class="navbar-item">
              Jobs
            </a>
            <hr class="navbar-divider">
            <a class="navbar-item">
              Contact
            </a>
          </div>
        </div>
      </div>

      <div class="navbar-end">
        <div class="navbar-item">
          <div class="buttons">
            <a
              href="https://github.com/jonathangoulding"
              class="button is-white"
            >
              <span class="icon">
                <i class="fab fa-github-square" />
              </span>
            </a>
            <a
              href="https://gitlab.com/jonathangoulding?nav_source=navbar"
              class="button is-white"
            >
              <span class="icon">
                <i class="fab fa-gitlab" />
              </span>
            </a>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data () {
    return {
      isActive: false,
      showNavbar: true
    }
  }
}
</script>
