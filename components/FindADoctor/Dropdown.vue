<template>
  <div>
    <v-container>
      <v-layout align-center>
        <v-flex md4 class="text-center">
          <h1 class="my_red--text">Find A Doctor</h1>
        </v-flex>
        <v-flex md4>
          <v-select
            :items="dropdown_font"
            label="Select Doctor"
            class="rounded-xl orange"
            color="red"
            background-color="blue"
            item-color="green"
            dense
          ></v-select
        ></v-flex>
        <v-flex md4>
          <v-overflow-btn
            :items="dropdown_font"
            label="Select Doctor"
            class="black rounded-xl"
          ></v-overflow-btn
        ></v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dropdown_font: [
        { text: "Internal med" },
        { text: "Calibriolog med" },
        { text: "Main med" },
        { text: "Verdana" },
      ],
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" scoped>
</style>