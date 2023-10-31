<script>

import { onMounted } from 'vue';

export default {
  setup() {
    onMounted(() => {
      console.log('here we are in onMonted');
    })
  }
}
</script>

<template>
    <div>
        Something in Home 01
    </div>
</template>