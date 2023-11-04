<script>
import { ref, toRefs, computed } from 'vue';

export default {
  props: {
    firstName: String,
    lastName: String,    
  },
  setup(props) {
    // const firstName = ref("Naty");
    // const lastName = ref("Gimenez");

    const { firstName, lastName } = toRefs(props);

    const fullName = computed(() => {
      return `${firstName.value} ${lastName.value}`;
    });

    return {
      firstName,
      lastName,
      fullName     
    }
  }
}
</script>

<template>
  <div>First Name: {{ firstName }}</div>
  <div>Last Name: {{ lastName }}</div>
  <div>Full Name: {{ fullName }}</div>
</template>