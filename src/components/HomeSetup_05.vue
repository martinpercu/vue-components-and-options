<script setup>
import { ref, computed, toRefs } from 'vue';

const props = defineProps({
    firstName: String,
    lastName: String,  
})

const { firstName, lastName } = toRefs(props);

// const firstName = ref("Naty");
// const lastName = ref("Gonzalez");

const fullName = computed(() => {
    return `${firstName.value} ${lastName.value}`;
});

</script>


<template>
    <div>First Name: {{ firstName }}</div>
    <div>Last Name: {{ lastName }}</div>
    <div>Full Name: {{ fullName }}</div>
</template>