<template>
  <div>
    <h1>Products</h1>
    <div v-for="product in products" :key="product.name">{{product.name}}
      <img alt="Phone" :src="product.image" />
      <div>{{product.cost}}</div>
      <button type="button" v-on:click="counter(product)">Add to cart</button>
    </div>   
  </div>
</template>
<script>
export default {
  name: "App",
  data() {
    return {
      products: [
        {
          name: "iphone 12 pro",
          cost: "prize 1,20,000",
          image: require("@/assets/iphone.jpg"),
          counter: 0
        }
      ]
    };
  },

  components: {}
};
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
} */
/* img {
  width: 20%;
  height: 10%;
  text-align: left;
}
.cart {
  width: 5%;
  padding: 10px 10px;
  margin-left: 50%;
  background-color: gray;
}
h1 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  font-size: 40px;
  margin-left: 5%;
}
p {
  font-size: 20px;
  font-weight: bold;
  margin-left: 5%;
}
button {
  margin-left: 5%;
} */
</style>
