<template>

  <b-navbar toggleable="lg" type="dark" variant="info">
    <b-navbar-brand :to="{name:'HOME'}">Producti</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item :to="{name:'ALL_PRODUCTS'}">Get All Products</b-nav-item>
        <b-nav-item :to="{name:'BY_ID'}" >Get Product By Id</b-nav-item>
        <b-nav-item :to="{name:'SEARCH'}" >Search</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
  name: "NavBar"
}
</script>

<style scoped>

</style>