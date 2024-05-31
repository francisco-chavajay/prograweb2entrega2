<!-- En este ejemplo, fullName es una propiedad computada que se actualiza automáticamente cuando firstName o lastName cambian. -->
<template>
    <div>
      <p>Full Name: {{ fullName }}</p>
    </div>
  </template>
  
  <script>
  import { ref, computed } from 'vue';
  
  export default {
    setup() {
      const firstName = ref('Francisco');
      const lastName = ref('Chavajay');
  
      const fullName = computed(() => `${firstName.value} ${lastName.value}`);
  
      return { firstName, lastName, fullName };
    }
  };
  </script>
