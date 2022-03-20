<template>
  <h1>Single Page</h1>
  <Header v-bind:cart="cart" />
</template>

<script>
import Header from "@/components/Header";
export default {
  name: "Single",
  data() {
    return {};
  },
  components: {
    Header,
  },
};
</script>