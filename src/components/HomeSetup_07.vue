<script setup>
import { computed, toRefs, inject } from 'vue';

const props = defineProps({
    firstName: String,
    lastName: String,  
})

const { firstName, lastName } = toRefs(props);

const fullName = computed(() => {
    return `${firstName.value} ${lastName.value}`;
});

const username = inject("theUsername");

</script>


<template>
    <div>First Name: {{ firstName }}</div>
    <div>Last Name: {{ lastName }}</div>
    <div>Full Name: {{ fullName }}</div>
  <div>NICK Name: {{ username }}</div>
</template>