<template>
  <b-container>
    <br>
    <b-jumbotron header="Producti" lead="Welcome to Producti frontend">

      <b-button class="mt-2" variant="primary" :to="{name:'ALL_PRODUCTS'}">Get All Products</b-button> <br>
      <b-button class="mt-2" variant="primary" :to="{name:'BY_ID'}">Get Product By Id</b-button> <br>
      <b-button class="mt-2" variant="primary" :to="{name:'SEARCH'}">Search Product</b-button> <br>
    </b-jumbotron>


  </b-container>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
  }
}
</script>
