<script>
import { ref, toRefs, computed, inject, watch } from 'vue';

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

    const myBtn = ref(null);

    console.log(myBtn.value);

    watch(myBtn, (theValue) => {
      console.log(theValue);
    })

    return {
      firstName,
      lastName,
      fullName,
      username,
      myBtn
    }
  }
}
</script>

<template>
  <div>First Name: {{ firstName }}</div>
  <div>Last Name: {{ lastName }}</div>
  <div>Full Name: {{ fullName }}</div>
  <div>NICK Name: {{ username }}</div>
  <button ref="myBtn">Click Me</button>
</template>