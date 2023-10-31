<script>
import { ref, reactive, watch } from 'vue';

export default {
  setup() {
    const counter = ref(10);
    const counterObject = reactive({ counter: 20 });

    setInterval(() => counter.value++, 2850);
    setInterval(() => counterObject.counter++, 1750);

    watch(counter, (newValue, oldValue) => {
        console.log(newValue, oldValue , "script OLD");
    });

    watch(() => counterObject.counter, (newValue, oldValue) => {
        console.log(newValue, oldValue , "script OLD this is counterObject");
    });



    return {
        counter,
        counterObject
    }
  }
}
</script>

<template>
    <div>Counter each 2850: {{ counter }}</div>
    <div>Counter Object using "reactive"  ==>  {{ counterObject }}</div>
</template>