<template>
  <div id="createItem">
    <h2>Create a new Item that is a Banana</h2>
    <input v-model="itemNameToCreate" placeholder="enter a new item name">
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
      console.log(this.itemNameToCreate)
      axios
        .post('http://localhost:8080/items', {'name': this.itemNameToCreate})
    }
  }
}
</script>

<style scoped>
</style>
