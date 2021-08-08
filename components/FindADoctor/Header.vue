<template>
  <div>
    <v-container>
      <v-layout align-center class="mt-6">
        <v-flex md4 class="text-center">
          <h1 class="my_red--text">Find A Doctor</h1>
        </v-flex>
        <v-flex md4 v-for="item in items" :key="item">
          <Dropdown :items="item" />
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
import Dropdown from "./Dropdown.vue";
export default {
  components: { Dropdown },
  data() {
    return {
      items: [
        ["Internal med", "Calibriolog med", "Main med", "Verdana"],
        ["Pristina", "mitrovica", "pec", "prizren", "leposavic"],
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
</style>