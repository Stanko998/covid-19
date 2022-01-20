<template>
  <div>
    <v-select :items="items" label="Filled style" light></v-select>
    <select name="color">
      <option value="">Select color</option>
      <option :value="item" v-for="item in items" :key="item">
        {{ item }}
      </option>
    </select>
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      items: ["crvena", "zelena", "plava"],
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" >
.v-select__selection.v-select__selection--comma,
.v-select.v-text-field input {
  color: green !important;
}
.theme--light.v-select .v-select__selections {
  color: green !important ;
}
</style>