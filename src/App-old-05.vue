<script>
import Home from './components/Home.vue';
import HomeSetup from './components/HomeSetup.vue';
import { provide } from 'vue';

export default {
  name: "App",
  components: {
    Home,
    HomeSetup
  },
  setup() {
    provide("theUsername", "PeteMar");
  }
}
</script>

<template>
  <div class="boldText"><br>export default<br></div>
  <Home first-name="Pedro" last-name="Mendoza" anAttribute="whatever"></Home>

  <div class="boldText"><br><br>script setup<br></div>
  <HomeSetup first-name="Peter" last-name="Marshall"></HomeSetup>

</template>

<style scoped>
.boldText {
  font-family: 'Courier New', Courier, monospace;
  font-weight: 800;
  font-size: x-large;
  padding-bottom: 5px;
}
</style>
