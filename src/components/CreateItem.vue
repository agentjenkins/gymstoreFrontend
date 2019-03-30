<template>
  <div id="createItem">
    <p>button</p>
    <button v-on:click="post">Post</button>
  </div>
</template>

<script>
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
    }
  }
}
</script>

<style scoped>
</style>
