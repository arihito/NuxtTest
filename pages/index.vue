<template>
  <section class="container">
    <div>
      <logo class="logo" />
      <h1 class="title">
        Nuxt.js Test
      </h1>
      <h2 class="subtitle">
        My amazing Nuxt.js project
      </h2>
      <hello :title="indexTitle">
        <!-- slot読み込み範囲 -->
        <div class="come">
          slot Test
        </div>
        <blockquate>
          Let us know how we did. All the tools your team needs in one place. Slack: Where work happens.
        </blockquate>
      </hello>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green">Documentation</a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey">GitHub</a>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Hello from '~/components/Hello.vue'

export default {
  components: {
    Logo,
    Hello
  },
  data() {
    return {
      indexTitle: 'Nuxt.js'
    }
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #6d5d30;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #5f5026;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
.come {
  color: #5f5026;
  font-size: 24px;
  margin-bottom: 20px;
  padding: 10px 30px;
  background-color: #0c141d;
  border-top: 2px solid rgb(182, 13, 13);
  border-bottom: 8px solid rgb(182, 13, 13);
}
blockquote {
  font-size: 8px;
}
</style>
