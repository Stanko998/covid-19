<template>
  <div>
    <Info />
    <v-container>
      <v-row justify="center">
        <v-btn large class="my_red my-6 headline py-9 font-weight-medium"
          >CORONAVIRUS AROUND THE WORLD</v-btn
        >
      </v-row>
    </v-container>
    <Map />
  </div>
</template>

<script>
import Info from "../components/Covid-19/Info.vue";
import Map from "../components/Covid-19/Map.vue";
export default {
  components: { Info, Map },
  data() {
    return {
      img: "Images/Covid-19/map.svg",
    };
  },
};
</script>

<style lang="scss" scoped>
.headline {
  font-family: "Montserrat", sans-serif !important;
}
</style>