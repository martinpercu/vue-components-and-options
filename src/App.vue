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
  <Home></Home>  
  <div><br><br></div>
  <HomeSetup></HomeSetup>

</template>

<style scoped>
</style>
