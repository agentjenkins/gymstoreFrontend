<template>
  <div id="createItem">
    <p>button</p>
    <button v-on:click="post">Post</button>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'CreateItem',
  data () {
    return {
      name: 'Vue.js'
    }
  },
  methods: {
    post: function (event) {
      console.log('banan')
      axios
        .post('http://localhost:8080/items', {'name': 'banan'})
    }
  }
}
</script>

<style scoped>
</style>
