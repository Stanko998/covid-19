<template>
  <div class="black--text">
    <v-select light :items="items" label="Standard" style="color: red">
    </v-select>
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      items: ["red", "green"],
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" scoped>
</style>
