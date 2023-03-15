<template>
  <Navbar />
  <router-view />
</template>

<script>
import Navbar from "@/components/Navbar.vue";

export default {
  name: "root",
  components: {
    Navbar,
  },
};
</script>

<style lang="scss">
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

body {
  box-sizing: border-box;
}
</style>
