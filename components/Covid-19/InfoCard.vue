<template>
  <div>
    <v-container row style="height: 130px">
      <v-row class="white">
        <v-col cols="2" class="text-center" :class="infocard.color">
          <v-icon class="" style="height: 100%" x-large>
            {{ infocard.icon }}</v-icon
          >
        </v-col>
        <v-col
          align-self="center"
          cols="10"
          class="font-weight-bold headline grey--text text--darken-2"
        >
          <v-col class="pa-0 ma-0">
            <span class="my_red--text">{{ infocard.span }} </span>
          </v-col>
          <v-col class="pa-0 ma-0">
            {{ infocard.body }}
          </v-col>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: ["infocard"],
};
</script>

<style lang="scss" scoped>
.display-1,
.headline {
  font-family: "Montserrat", sans-serif !important;
}
.container .row {
  &:hover {
    box-shadow: 5px 5px 15px black;
    cursor: pointer;
  }
}
</style>