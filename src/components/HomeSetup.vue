<script setup>
import { ref, computed } from 'vue';

const firstName = ref("Naty");
const lastName = ref("Gimenez");

const fullName = computed(() => {
    return `${firstName.value} ${lastName.value}`;
});

</script>


<template>
    <div>First Name: {{ firstName }}</div>
    <div>Last Name: {{ lastName }}</div>
    <div>Full Name: {{ fullName }}</div>
</template>