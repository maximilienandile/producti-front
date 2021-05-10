<template>
  <b-container>
    <h2>All products</h2>
    <b-button variant="success" @click="getAll">Get All Products</b-button>
    <hr>
    <h4>Result:</h4>
    <ul class="list-group">
      <li v-for="(product, idx) in products" :key="idx" class="list-group-item">{{ product.name }} ({{product.id}})</li>
    </ul>
    <hr>
    <h4>Raw Result : </h4>
    <pre>{{products}}</pre>
  </b-container>
</template>

<script>
import axios from "axios";

export default {
name: "AllProducts",
  data() {
    return {
     products: null
    }
  },
  methods: {
    getAll(){
      axios.get(process.env.VUE_APP_API_BASE_URL + '/products').then((res)=>{
        this.products = res.data
      }).catch((err)=>{
        alert("Unexpected error "+err)
      })
    },
  }
}
</script>

<style scoped>

</style>