<template>
  <div class="content is-medium">
    <article>
      <nuxt-content :document="article" />
    </article>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const article = await $content('articles', params.slug).fetch()

    return { article }
  }
}
</script>

<style>
.icon.icon-link {
  background-image: url('/images/svg/icon-link.svg');
  display: inline-block;
  width: 20px;
  height: 20px;
  background-size: 20px 20px;
}
</style>
