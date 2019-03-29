<template>
  <div>
    <ul id='kalle'>
      <li v-for="(item) in items" v-bind:key="item.name">{{item.name}}</li>
    </ul>
    <p>{{items}}</p>
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
