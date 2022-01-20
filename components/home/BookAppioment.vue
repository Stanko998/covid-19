<template>
  <v-btn class="rounded-lg ml-2 my_red" :class="info">Book Appioment</v-btn>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: ["info"],
};
</script>

<style lang="scss" scoped>
.v-btn {
  text-transform: none;
}
</style>