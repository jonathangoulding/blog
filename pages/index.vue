<template>
  <div>
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
    <!-- newsletter -->
    <section class="section">
      <div class="columns">
        <div class="column is-10 is-offset-1">
          <div class="container has-text-centered is-fluid">
            <div class="hero is-light">
              <div class="hero-body">
                <h2 class="title is-4">
                  Find me on:</h1>
                  <div class="columns is-mobile is-centered">
                    <div class="column is-half">
                      <div class="columns is-mobile">
                        <div class="column">
                          <a href="https://github.com/jonathangoulding">
                            <span class="icon">
                              <i class="fab fa-github-square" />
                            </span>
                          </a>
                        </div>
                        <div class="column">
                          <a href="https://gitlab.com/jonathangoulding?nav_source=navbar">
                            <span class="icon">
                              <i class="fab fa-gitlab" />
                            </span>
                          </a>
                        </div>
                        <div class="column">
                          <a href="https://www.linkedin.com/in/jonathan-goulding-78a5a4114/">
                            <span class="icon">
                              <i class="fab fa-linkedin" />
                            </span>
                          </a>
                        </div>
                      </div>
                    </div>
                  </div>
                </h2>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Articles -->
    <section class="hero ">
      <div class="hero-body">
        <div class="container">
          <section id="group-1" class="section">
            <div class="columns is-variable is-8">
              <div class="column is-5 is-offset-1 ">
                <div class="content is-medium">
                  <h2 class="subtitle is-5 has-text-grey">
                    March 10, 2021
                  </h2>
                  <h1 class="title has-text-black is-3">
                    Orchestrating pipelines <a href="#group-1"><i
                      class="fas fa-link fa-xs"
                    /></a>
                  </h1>
                  <p class="has-text-dark">
                    I am currently working towards an orchestated docker system
                    using gitlab ci to
                    make composable gitlab ci jobs that can be used through multiple project.
                    The jobs (mainly test) can pull the orechestraion repository and use the docker
                    compose to stand up the system
                    in order to test it in the pipeline.
                  </p>
                </div>
              </div>
              <div class="column is-5">
                <div class="content is-medium">
                  <h2 class="subtitle is-5 has-text-grey">
                    Febuary 5, 2021
                  </h2>
                  <h1 class="title has-text-black is-3">
                    Devil donuts webiste <a href="#group-1"><i
                      class="fas fa-link fa-xs"
                    /></a>
                  </h1>
                  <p class="has-text-dark">
                    Yes, the Devil Donuts company from The Simpsons episode <a
                      href="https://simpsons.fandom.com/wiki/The_Day_the_Earth_Stood_Cool"
                    > "The Day
                      the Earth Stood Cool"</a>.
                    I wanted to explore <a href="https://vuepress.vuejs.org/">Vuepress</a> with Netlify
                    CMS and have a bit of fun with it.
                    The main site is hosted on <a
                      href="https://devildonuts.demonicfridge.com"
                    >devildonuts.demonicfridge.com</a>.
                  </p>
                  <p class="has-text-dark">
                    I enjoyed making the site and attempting to bundle a buiness site and blog in one
                    project.
                    I tried to make a <a
                      href="https://devildonuts.demonicfridge.com/about/ingredients.html"
                    > Devil
                      Donuts ingredients chart </a> using <a
                      href="https://www.chartjs.org/docs/latest/"
                    >chart.js</a>.
                    I think we can agree its not what i had in mind.
                    Buts its good to fail and make mistakes otherwise we would never learn.
                  </p>
                </div>
              </div>
            </div>
          </section>
          <div class="is-divider" />
          <section class="section">
            <div class="columns is-variable is-8">
              <div class="column is-5 is-offset-1">
                <div class="content is-medium">
                  <h2 class="subtitle is-5 has-text-grey">
                    December 25, 2018
                  </h2>
                  <h1 class="title has-text-black is-3">
                    Lorem ipsum dolor sit amet <i
                      class="fas fa-tools fa-xs"
                    />
                  </h1>
                  <p class="has-text-dark">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                    eiusmod tempor incididunt ut labore et dolore magna aliqua.
                    Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip
                    ex ea commodo consequat.
                    Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
                    fugiat nulla pariatur.
                    Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt
                    mollit anim id est laborum.
                  </p>
                </div>
              </div>
              <div class="column is-5">
                <div class="content is-medium">
                  <h2 class="subtitle is-5 has-text-grey">
                    December 25, 2018
                  </h2>
                  <h1 class="title has-text-black is-3">
                    Lorem ipsum dolor <i
                      class="fas fa-tools fa-xs"
                    />
                  </h1>
                  <p class="has-text-dark">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                    eiusmod tempor incididunt ut labore et dolore magna aliqua.
                    Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip
                    ex ea commodo consequat.
                    Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
                    fugiat nulla pariatur.
                    Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt
                    mollit anim id est laborum.
                  </p>
                </div>
              </div>
            </div>
          </section>
        </div>
      </div>
    </section>
  </div>
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
