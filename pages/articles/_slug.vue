<template>
  <div class="content is-medium">
    <article>
      <button
        class="button is-text"
        style="
        color: grey;
        text-decoration: none;"
        @click="$router.go(-1)"
      >
        <i class="fas fa-arrow-left" />
      </button>
      <h2 class="subtitle is-4">
        {{ formatDate(article.updatedAt) }}
      </h2>
      <h1 class="title">
        {{ article.title }}
      </h1>
      <nuxt-content :document="article" />
    </article>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const article = await $content('articles', params.slug).fetch()

    return { article }
  },
  methods: {
    formatDate (date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    }
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
