<template>
  <b-container>
    <br>
    <b-jumbotron header="Producti" lead="Welcome to Producti frontend">

      <b-button variant="primary" :to="{name:'ALL_PRODUCTS'}">Get All Products</b-button>
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
