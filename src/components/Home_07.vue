<script>
import { toRefs, computed, inject } from 'vue';

export default {
  props: {
    firstName: String,
    lastName: String,    
  },
  setup(props, { expose }) {

    const { firstName, lastName } = toRefs(props);

    const fullName = computed(() => {
      return `${firstName.value} ${lastName.value}`;
    });

    const username = inject("theUsername");

    expose({
      fullName,
    });

    return {
      firstName,
      lastName,
      fullName,
      username
    }
  }
}
</script>

<template>
  <div>First Name: {{ firstName }}</div>
  <div>Last Name: {{ lastName }}</div>
  <div>Full Name: {{ fullName }}</div>
  <div>NICK Name: {{ username }}</div>
</template>