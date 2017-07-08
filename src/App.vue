<template>
  <div id="app">
    <img id="logo" src="./assets/logo.png" v-scroll-to="'#element'">
    
    <div v-for="i in 400" :key="i"
         style="height: 50px;
                display: block;
                background: #42b983;
                border-bottom: 1px solid #eee;"></div>

    <div id="element" v-scroll-to="'#logo'">
      Hi I'm #element
    </div>

  </div>
</template>

<script>
export default {
  name: 'app',
  mounted() {
    this.$scrollTo('#element', 1000, { easing: 'ease', cancelable: false })

  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
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
