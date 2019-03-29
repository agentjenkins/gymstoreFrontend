<template>
  <div>
    <h1>{{item}}</h1>
    <h2>{{name}}</h2>
  </div>
</template>

<script>
export default {
  name: 'item',
  data () {
    return {
      item: 'Bars',
      name: 'superBar'
    }
  }
}
</script>

<style scoped>

</style>
