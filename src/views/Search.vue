<template>
  <b-container>
    <h2>Search products</h2>
    <b-form-input v-model="name" placeholder="Enter a product name"></b-form-input>
    <br>
    <b-button variant="success" @click="getAll">Search</b-button>
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
      name: null,
      products: null,
      showAlert: false,
      alertText:null

    }
  },
  methods: {
    getAll(){
      if (this.name === null){
        alert("please input a name")
        return
      }
      axios.get(process.env.VUE_APP_API_BASE_URL + '/product?search='+this.name).then((res)=>{
        this.products = res.data
      }).catch((err)=>{
        if (err.response.status === 404){
          alert("No results found")
        } else {
          alert("Unexpected error "+err)
        }
      })
    },
  }
}
</script>

<style scoped>

</style>