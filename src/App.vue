<template>
  <router-view />
</template>

<script>
import { defineComponent } from "vue";

window.location.reload(true);
console.log(window.location.reload(true));

export default defineComponent({
  name: "App",
});
</script>
