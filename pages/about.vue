<template lang="html">
  <div>
    <header>
      <h1>Nuxt.js ハンズオン</h1>
      <nuxt-link 
        to="/" 
        class="button--green">TOP</nuxt-link>
      <nuxt-link 
        to="/about" 
        class="button--green">ABOUT</nuxt-link>
      <nuxt-link 
        to="/service" 
        class="button--green">SERVICE</nuxt-link>
      <nuxt-link 
        to="/contact" 
        class="button--green">CONTACT</nuxt-link>
    <div class="slot"/></header>
    <nuxt />
    <footer><p>2018.11.17</p></footer>
  </div>
</template>
​
<script>
export default {
  head() {
    return {
      // タイトルテンプレートがある場合は "ABOUT - ポートフォリオ" になる
      title: 'ABOUT',
      // タイトルのテンプレートを定義することもできる
      titleTemplate: '%s - ポートフォリオ',
      meta: [
        { hid: 'description', name: 'description', content: 'About ページ' }
      ]
    }
  }
}
</script>
​
<style lang="scss">
</style>
