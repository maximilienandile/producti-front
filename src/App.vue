<template>
  <b-container fluid=""  id="app">
    <NavBar></NavBar>
    <router-view/>
  </b-container>
</template>

<script>
import NavBar from "@/components/NavBar";
export default {
  components: {NavBar}
}
</script>