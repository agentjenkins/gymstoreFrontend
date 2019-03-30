<template>
  <div>
    <h1>Item List</h1>
    <ul id='itemList'>
      <li v-for="(item) in items" v-bind:key="item.id">{{item.name}}</li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'Items',
  data () {
    return {
      items: null
    }
  },
  mounted () {
    axios
      .get('http://localhost:8080/items')
      .then(response => (this.items = response.data))
  }
}
</script>

<style scoped>
</style>
