<template>
  <div>
    <ul id="kalle">
      <li v-for="(item) in items" v-bind:key="item.name">
        {{item.name}}
      </li>

    </ul>
  </div>
</template>

<script>
export default {
  name: 'Items',
  data () {
    return {
      items: [
        {name: 'chocklad'},
        {name: 'Bar'}
      ]
    }
  }
}
</script>

<style scoped>

</style>
