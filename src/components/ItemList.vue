<template>
  <div>
    <h1>Item List</h1>
    <ul id='itemList'>
      <li v-for="(item) in items" v-bind:key="item.id"><button v-on:click="buyItem(item)">Buy {{item.name}}</button></li>
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
  },
  methods: {
    buyItem: function (item) {
      console.log(item.id)
      axios.post('http://localhost:8080/purchases', {'userId': 'thomas', 'itemId': item.id})
    }
  }
}
</script>

<style scoped>
</style>
