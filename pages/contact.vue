<template lang="html">
  <div>
    <header>
      <h1>Nuxt.js ハンズオン</h1>
      <nuxt-link to="/">TOP</nuxt-link>
    </header>
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
