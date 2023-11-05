<script>
import { toRefs, computed } from 'vue';

export default {
  props: {
    firstName: String,
    lastName: String,    
  },
  setup(props, { expose }) {
  // setup(props, context) {

    // console.log(context);

    const { firstName, lastName } = toRefs(props);

    const fullName = computed(() => {
      return `${firstName.value} ${lastName.value}`;
    });

    expose({
      fullName,
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