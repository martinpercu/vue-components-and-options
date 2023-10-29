<script>
import Menu from './components/Menu.vue';

export default {
  name: "App",
  components: { Menu },
  data() {
    return {
      showed: false
    }
  }
}

</script>

<template>
  <button @click="showed = !showed">Menu</button>
  <transition name="fadeMenu">  
    <Menu v-show="showed" />
  </transition>
</template>

<style scoped>
.fadeMenu-enter-from {
  border: 2px solid green;

}
.fadeMenu-enter-active {
  border: 2px solid blue;
}
.fadeMenu-enter-to {
  border: 2px solid red;
}
.fadeMenu-leave-from {
  border: 2px solid rgb(47, 78, 75);
}
.fadeMenu-leave-active {
  border: 2px solid rgb(14, 133, 108);
}
.fadeMenu-leave-to {
  border: 2px solid rgb(182, 89, 192);
}
.fadeMenu-leave-active,
.fadeMenu-enter-active {
  transition: opacity 1.4s ease;
}
.fadeMenu-leave-to,
.fadeMenu-enter-from {
  opacity: 0;
}
</style>
