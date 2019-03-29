<template>
  <div>
    <ul id="kalle">
      <li v-for="(item) in items" v-bind:key="item.name">{{item.name}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Items",
  data() {
    return {
      items: [
        {
          id: "fadd89bd-fae4-4111-b0ba-3fed2c76afdd",
          name: "Snacks"
        },
        {
          id: "f5a9d3ea-41bf-47c5-8c16-f043ec4ee5bf",
          name: "dddd"
        },
        {
          id: "b1dd3978-3de2-4815-80ab-7dc68c6c6838",
          name: "babbs"
        },
        {
          id: "b93eb25b-7d18-4d4e-8d89-8e0e9003d629",
          name: "smör"
        }
      ]
    };
  }
};
</script>

<style scoped>
</style>
