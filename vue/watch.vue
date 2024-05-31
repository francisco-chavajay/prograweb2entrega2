<!-- En este ejemplo, el watcher observa los cambios en count y actualiza previousCount con el valor anterior de count cada vez que cambia. -->
<template>
    <div>
      <p>Count: {{ count }}</p>
      <p>Previous Count: {{ previousCount }}</p>
      <button @click="increment">Increment</button>
    </div>
  </template>
  
  <script>
  import { ref, watch } from 'vue';
  
  export default {
    setup() {
      const count = ref(0);
      const previousCount = ref(0);
  
      const increment = () => {
        count.value++;
      };
  
      watch(count, (newVal, oldVal) => {
        previousCount.value = oldVal;
      });
  
      return { count, previousCount, increment };
    }
  };
  </script>
