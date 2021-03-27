<template>
  <section class="hero">
    <div class="hero-body">
      <div class="container">
        <div class="is-divider" />
        <BlogSnippet
          title="Simple mini blog introduction"
          date="March 5, 2021"
        >
          <p>
            This is a simple mini blog.
            Currently hard coded html with a future view to use vuepress with a custom theme,
            vue or nuxt.
            For now the simplicity of hard coding the small articles and using the bulma and
            font awesome cdn is sufficent.
          </p>
        </BlogSnippet>
        <BlogSnippet
          title="That side project domain you always use... "
          date="March 11, 2021"
        >
          <p>
            I use the <a href="https://demonicfridge.com/">demonicfridge.com</a> domain for my
            side projects that require a domain name.
            I find just having the domain makes things easier to develop and test.
            For example <a
              href="https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-16-04"
            >securing
              nginx with let's encrypt</a> .
          </p>
        </BlogSnippet>
        <BlogSnippet
          title="Deploying a vuepress site to GitHub Pages"
          date=" March 5, 2021"
        >
          <p>
            I wanted to explore Github actions and understand how to deploy a website that has a
            build step.
            I had read a few tutorial that did some complicated things. Some even required
            multiple 'marketplace' actions.
            This seemed too complicated. So i tried to make it work with just a GitHub action
            and config for my <a href="https://github.com/jonathangoulding/vuepress-docs-example"> Vuepress Doc
              Example</a> repo.
          </p>
          <button class="button is-outlined gh-pages-action-code-acc" @click="viewGitHubAction = !viewGitHubAction">
            View Github Action
          </button>
          <img v-if="viewGitHubAction" src="~assets/images/vuepress-github-action.svg" alt="" srcset="">
        </BlogSnippet>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      viewGitHubAction: false
    }
  }
}
</script>
