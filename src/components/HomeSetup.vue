<script setup>

import { ref, reactive, watch } from 'vue';
const counter = ref(10);
const counterObject = reactive({ counter: 20 });

setInterval(() => counter.value++, 1250);
setInterval(() => counterObject.counter++, 750);

watch(counter, (newValue, oldValue) => {
    console.log(newValue, oldValue);
});

watch(() => counterObject.counter, (newValue, oldValue) => {
    console.log(newValue, oldValue , "this is counterObject");
});

</script>



<template>
    <div>Counter each 1250: {{ counter }}</div>
    <div>Counter Object using "reactive"  ==>  {{ counterObject }}</div>
</template>