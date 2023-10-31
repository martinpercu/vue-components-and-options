<script>
import one_example_01 from "../src/mixins/example_01";
import another_example from "../src/mixins/example_02";

export default {
  name: "App",
  mixins: [one_example_01, another_example],
  data() {
    return {
      text: "bonjour Le Monde",
      something2: "this is in the app.vue in line 11 , if you comment this line I will show the var in the MIXIN ! ! !"
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
  <div> {{  something }}</div>
  <div style="font-weight: 800;"> {{  something2 }}</div>
  
</template>



<style scoped>

</style>
