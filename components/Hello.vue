<template lang="html">
  <div class="hello">
    Hello, I'm {{ name }}! {{ title }} on {{ place }} {{ reverseName }}<br>
    <button 
      class="button"
      type="button" 
      name="button"
      @click="plus">クリック回数: <span class="num">{{ num }}</span></button>
    <div :class="['hide', { seven: num === 3 }]">
      3回クリックしたよ！
    </div>
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
    <div class="slot">
      <slot />
    </div>
  </div>
</template>
​
<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Nuxt.js-Handson!!'
    }
  },
  data() {
    return {
      name: 'Arihito',
      place: 'Zozo',
      num: 0
    }
  },
  computed: {
    reverseName() {
      return this.name
        .split('')
        .reverse()
        .join('')
    }
  },
  methods: {
    plus() {
      this.num++
    }
  }
}
</script>
​
<style lang="scss" scoped>
.hello {
  margin: 20px 0;
  color: #5f5026;
  padding: 10px;
  background: linear-gradient(#0c141d, #060f14);
  border-radius: 5px;
}
.button {
  height: 50px;
  margin: 10px 0;
  padding: 10px 30px;
  border: 1px solid rgb(60, 122, 60);
  background-color: #0c141d;
  border-radius: 3px;
  color: rgb(60, 122, 60);
  font-size: 18px;
  text-decoration: none;
}
.button:focus {
  border: none;
  box-shadow: none;
}
.button:hover {
  background-color: rgb(83, 143, 118);
  color: #fff;
}
.num {
  font-weight: bold;
}
.hide {
  display: none;
  &.seven {
    display: block;
    font-size: 18px;
    font-weight: bold;
  }
  &.seven::first-letter {
    font-size: 42px;
    margin: -10px 5px 0 0;
  }
}
</style>
