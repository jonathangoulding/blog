<template>
  <section class="hero">
    <div class="hero-body">
      <div class="container">
        <BlogSnippet
          title="Orchestrating pipelines "
          date="March 5, 2021"
        >
          <p>
            I am currently working towards an orchestated docker system
            using gitlab ci to
            make composable gitlab ci jobs that can be used through multiple project.
            The jobs (mainly test) can pull the orechestraion repository and use the docker
            compose to stand up the system
            in order to test it in the pipeline.
          </p>
        </BlogSnippet>
        <BlogSnippet
          title="Devil donuts webiste"
          date="Febuary 5, 2021"
        >
          <p>
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
          <p>
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
        </BlogSnippet>
      </div>
    </div>
  </section>
</template>
