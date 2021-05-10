<template>
  <b-container>
    <h2>Product By Id</h2>
    <b-form-input v-model="productId" placeholder="Enter a product ID"></b-form-input>
    <br>
    <b-button variant="success" @click="getAll">Get Product</b-button>
    <hr>
    <h4>Raw Result : </h4>
    <pre>{{product}}</pre>
  </b-container>
</template>

<script>
import axios from "axios";

export default {
  name: "ProductById",
  data() {
    return {
      productId: "",
      product : null
    }
  },
  methods: {
    getAll(){
      axios.get(process.env.VUE_APP_API_BASE_URL + '/product/'+this.productId).then((res)=>{
        this.product = res.data
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