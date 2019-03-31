@import "compass/css3";
<template>
  <div class="center" >
    <h1>Buy some Bars and Snacks</h1>
    <ul id='itemList' class="flex-container">
      <li class="flex-item" v-for="(item) in items" v-bind:key="item.id"><button v-on:click="buyItem(item)"> <img class="flex-item" src="../assets/nocco.png"> Buy {{item.name}}</button></li>
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
 .center {
    margin: auto;
    width: 30%;
    border: 3px solid lightblue;
    padding: 10px;
  }

.flex-container {
  flex-direction: row;
  flex-wrap: wrap;
  padding: 10;
  margin: 10;
  align: center;
  list-style: none;
  display: -webkit-box;
  display: -moz-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-flex-flow:  wrap;
  justify-content: flex-start;

}

.flex-item {
  padding: 5px;
  width: 75px;
  margin-top: 10px;
  flex-basis: 100px;

  line-height: 150px;
  color: white;
  font-weight: bold;
  font-size: 3em;
  text-align: center;
}

</style>
