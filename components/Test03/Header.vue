<template>
  <header>
    <h1>{{ title }}</h1>
    <Button />
  </header>
</template>

<script lang="ts">
import Button from "./Button.vue";

export default {
  name: "covid19Header",

  components: {
    Button,
  },

  props: ["title"],
};
</script>

<style lang="scss" scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
