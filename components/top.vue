<template>
  <section class="hero">
    <div class="hero-body">
      <div class="container">
        <div class="is-divider" />
        <section class="section">
          <div class="columns">
            <div class="column is-8 is-offset-2">
              <div class="content is-medium">
                <h2 class="subtitle is-4">
                  March 5, 2021
                </h2>
                <h1 class="title">
                  Simple mini blog introduction <a href="#"><i
                    class="fas fa-link fa-xs"
                  /></a>
                </h1>
                <p>
                  This is a simple mini blog.
                  Currently hard coded html with a future view to use vuepress with a custom theme,
                  vue or nuxt.
                  For now the simplicity of hard coding the small articles and using the bulma and
                  font awesome cdn is sufficent.
                </p>
              </div>
            </div>
          </div>
        </section>
        <section id="side-project" class="section">
          <div class="columns">
            <div class="column is-8 is-offset-2">
              <div class="content is-medium">
                <h2 class="subtitle is-4">
                  March 11, 2021
                </h2>
                <h1 class="title">
                  That side project domain you always use... <a href="#side-project"><i
                    class="fas fa-link fa-xs"
                  /></a>
                </h1>
                <p>
                  I use the <a href="https://demonicfridge.com/">demonicfridge.com</a> domain for my
                  side projects that require a domain name.
                  I find just having the domain makes things easier to develop and test.
                  For example <a
                    href="https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-16-04"
                  >securing
                    nginx with let's encrypt</a> .
                </p>
              </div>
            </div>
          </div>
        </section>
        <section id="vuepress-gh-pages" class="section">
          <div class="columns">
            <div class="column is-8 is-offset-2">
              <div class="content is-medium">
                <h2 class="subtitle is-4">
                  March 5, 2021
                </h2>
                <h1 class="title">
                  Deploying a vuepress site to GitHub Pages <a
                    href="#vuepress-gh-pages"
                  ><i class="fas fa-link fa-xs" /> </a>
                </h1>
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
              </div>
            </div>
          </div>
        </section>
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
