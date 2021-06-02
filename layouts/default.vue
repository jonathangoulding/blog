<template>
  <div>
    <div v-if="$route.path === '/'" class="hero-img">
      <section class="section">
        <div class="container hero-img-text">
          <h1 class="title has-text-white">
            Jonathan Goulding
          </h1>
          <h3 class="subtitle has-text-white">
            Software Engineer
          </h3>
        </div>
      </section>
    </div>
    <div class="section main">
      <h1 class="has-text-centered">
        <nuxt-link to="/">
          Home
        </nuxt-link> | <nuxt-link to="/blog">
          Blog
        </nuxt-link>
      </h1>
      <section class="section">
        <div class="columns">
          <div class="column is-8 is-offset-2">
            <Nuxt />
          </div>
        </div>
      </section>
    </div>
    <Footer />
  </div>
</template>

<style>
.main {
  display: flex;
  min-height: 80vh;
  flex-direction: column;
}

.section {
  flex: 1;
}

.hero-img {
  background-image: url("/images/public_img_backgrounds_grass-green-plants-natural.jpg");
  opacity: 0.7;
  background-color: #020202;
  height: 300px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}

.hero-img-text {
  text-align: center;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

a {
  color: grey;
  text-decoration: none;
}
</style>
