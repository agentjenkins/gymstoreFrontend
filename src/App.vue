<template>
  <div id="app">
    <Items/>
    <CreateItem/>
  </div>
</template>

<script>
import Items from './components/ItemList'
import CreateItem from './components/CreateItem'

export default {
  name: 'App',
  components: {
    Items,
    CreateItem
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
</style>
