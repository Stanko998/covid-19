<template>
  <div>
    <!--
    <select class="my_blue--text font-weight-bold display-1 pl-5 py-2">
      <option value="">Select color</option>
      <option :value="item" v-for="(item, i) in items" :key="item">
        {{ items[i] }}
      </option>
    </select>
    -->
    <v-select light :items="items" label="Standard" v-on:change="promena()">
    </v-select>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: ["items"],
  mounted() {
    let selects = document.querySelectorAll("label");
    selects.forEach((select) => {
      select.style.color = "green";
    });
  },

  methods: {
    promena() {
      console.log("promena");
      setTimeout(() => {
        let selects2 = document.querySelectorAll(".v-select__selection--comma");
        console.log(selects2);
        selects2[0].style.color = "blue";
      }, 100);
    },
  },
};
</script>

<style lang="scss" scoped>
/*
div {
  display: flex;
  select {
    margin: auto;
    box-shadow: 0 0 10px black;
    border-radius: 24px;
    width: 70%;
    &:focus-visible {
      outline: none;
      option:first-child {
        display: none;
      }
    }
  }
}
*/
</style>