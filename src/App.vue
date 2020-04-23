<template>
  <div id="app">
    <h1>App 组件</h1>
    <div>计数：{{ $store.state.count }}个</div>
    <div>getters计数：{{ $store.getters.count }}个</div>
    <button @click="add">commit加</button>
    <button @click="dispatchAdd">dispatch加</button>

    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  methods: {
    add() {
      this.$store.commit('ADD_COUNT', 100)
    },
    dispatchAdd() {
      this.$store.dispatch('addCount', 1)
    }
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
