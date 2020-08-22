<template>
  <div id="app" class="container">
    <Navigation></Navigation>

    <div class="top">
      <h1>Vue CLIを使って作ってみたSPA</h1>
      <h3>Cat Fact</h3>
      <p>
        axiosを使って<a href="https://alexwohlbruck.github.io/cat-facts/">cat-facts</a>から取得した猫の話を表示します
      </p>
      <blockquote id="cat-fact">
        {{ cat_fact }}
      </blockquote>
    </div>
  </div>
</template>

<script>
import Navigation from '@/components/Navigation.vue'
import axios from '@nuxtjs/axios'

export default {
  name: 'App',
  components: {
    Navigation
  },
  data: () => {
    return {
      cat_fact: 'loading'
    }
  },
  mounted: async function(){
    const response = await this.$axios.$get('https://cat-fact.herokuapp.com/facts/random')
    console.log(response);
    this.cat_fact = response.text
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
h3 {
  margin: 40px 0 0;
}
#cat-fact {
  padding: 1em;
  width: 40em;

  position: relative;
  left: calc(50% - 23em);
  background-color: darkgray;
}
</style>
