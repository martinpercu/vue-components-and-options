<script setup>
import { ref, computed, toRefs, inject, watch } from 'vue';

const props = defineProps({
    firstName: String,
    lastName: String,  
})

const { firstName, lastName } = toRefs(props);

const fullName = computed(() => {
    return `${firstName.value} ${lastName.value}`;
});

const username = inject("theUsername");

const myBtn = ref(null);

console.log(myBtn.value);

watch(myBtn, (theValue) => {
    console.log(theValue);
})

</script>


<template>
    <div>First Name: {{ firstName }}</div>
    <div>Last Name: {{ lastName }}</div>
    <div>Full Name: {{ fullName }}</div>
    <div>NICK Name: {{ username }}</div>
    <button ref="myBtn">Click Me Setup</button>
</template>