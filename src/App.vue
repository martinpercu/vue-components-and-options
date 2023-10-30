<script>
export default {
  name: "App",
  data() {
    return {
      text: "bonjour Le Monde"
    }
  },
  beforeCreate() {
    console.log("beforeCreate almost no info ", this.$data, this.$el);
  },
  created() {
    console.log("created only get the $data ===> text: \"bonjour... ", this.$data, this.$el);
  },
  mounted() {
    console.log("mounted now we have all the info from this element. ", this.$data, this.$el);
  }
}

</script>

<template>
  <div>{{ text }}</div>
  
</template>



<style scoped>

</style>
