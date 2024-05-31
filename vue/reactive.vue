<!-- En este ejemplo, user es un objeto reactivo. Sus propiedades son reactivas y pueden ser accedidas y modificadas directamente. -->
<template>
  <div>
    <p>{{ user.name }}</p>
    <button @click="changeName">Change Name</button>
  </div>
</template>

<script>
import { reactive } from "vue";

export default {
  setup() {
    const user = reactive({
      name: "Francisco Chavajay",
    });

    const changeName = () => {
      user.name = "Francisco Chavajay";
    };

    return { user, changeName };
  },
};
</script>
