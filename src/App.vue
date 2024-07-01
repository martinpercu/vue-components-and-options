<script>
import Home from './components/Home.vue';
import HomeSetup from './components/HomeSetup.vue';

export default {
  name: "App",
  components: {
    Home,
    HomeSetup
}
}
</script>

<template>
  <div class="boldText"><br>export default<br></div>
  <Home></Home>
  <div class="boldText"><br><br>script setup<br></div>
  <HomeSetup></HomeSetup>

</template>

<style scoped>
.boldText {
  font-family: 'Courier New', Courier, monospace;
  font-weight: 800;
  font-size: larger;
}
</style>
