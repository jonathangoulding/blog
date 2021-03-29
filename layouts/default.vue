<template>
  <div>
    <div class="hero-img">
      <section class="section">
        <div class="container hero-img-text">
          <h1 class="title has-text-white">
            Jonathan Goulding
          </h1>
          <h3 class="subtitle has-text-white">
            Software Engineer
          </h3>
          <h1 class="title has-text-white">
            Blog
          </h1>
        </div>
      </section>
    </div>
    <Nuxt />
  </div>
</template>

<style>
.hero-img {
  background-image: url("~assets/images/public_img_backgrounds_grass-green-plants-natural.jpg");
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
