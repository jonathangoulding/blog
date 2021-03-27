<template>
  <section class="section">
    <div class="columns">
      <div class="column is-8 is-offset-2">
        <div class="content is-medium">
          <h2 class="subtitle is-4">
            {{ date }}
          </h2>
          <h1 class="title">
            {{ title }}
          </h1>
          <slot />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: ['title', 'date', 'para']
}
</script>
