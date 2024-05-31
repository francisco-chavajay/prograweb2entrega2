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
      name: "John Doe",
    });

    const changeName = () => {
      user.name = "Jane Doe";
    };

    return { user, changeName };
  },
};
</script>
