<template>
  <div id="nav">
    <div id="title">
      <span>Vue CLIで試しに作ってみたページ</span>
    </div>
    <div id="pages">
      <ul>
        <li><NuxtLink to="/">Home</NuxtLink></li>
        <li><NuxtLink to="/about">About</NuxtLink></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Navigation',
  props: {
  }
}
</script>

<style scoped>
#nav {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

#title span {
  text-align: left;
  top: calc(50% - 1eh);
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
