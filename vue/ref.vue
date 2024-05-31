<!-- esto es un ejemplo de como podemos usar ref,  En este ejemplo, count es una referencia reactiva. Accedemos a su valor a través de count.value. -->
<template>
  <div>
    <p>{{ count.value }}</p>
    <button @click="increment">Increment</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const count = ref(0);

    const increment = () => {
      count.value++;
    };

    return { count, increment };
  },
};
</script>
