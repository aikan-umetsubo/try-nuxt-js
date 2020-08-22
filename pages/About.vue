<template>
  <div id="about" class="container">
    <Navigation></Navigation>

    <h1>このページについて</h1>
    <p>
      Vue CLIで試しにSPAを作ってみた。使っている技術は：
    </p>
    <ul>
      <li>Vue.js</li>
      <li>Vue CLI</li>
      <li>Vue Router</li>
      <li>axios</li>
    </ul>
  </div>
</template>

<style scoped>
#about {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
