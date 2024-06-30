<script setup>

import { ref, reactive } from 'vue';

const text = ref("This is the value text ");
const number = ref(4);
const counter = ref(0);
const counterObject = reactive({ counter: 20 });

setInterval(() => counter.value++, 650);
setInterval(() => counterObject.counter++, 1750);

</script>

<template>
    <div>{{ text }}</div>
    <div>{{ number }}</div>
    <div>Counter each 650: {{ counter }}</div>
    <div>Counter Object using "reactive"  ==>  {{ counterObject }}</div>
</template>