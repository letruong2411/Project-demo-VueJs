<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
	<ComponentHeader />
	<ListProducts />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import ComponentHeader from './components/ComponentHeader'
import ListProducts from './components/ListProducts'
export default {
  created () {
  },
  methods: {
  },
  name: 'App',
  components: {
	HelloWorld,
	ComponentHeader,
	ListProducts
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
  margin-top: 60px;
}
</style>
