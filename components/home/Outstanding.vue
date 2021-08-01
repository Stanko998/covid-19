<template>
  <div class="py-5">
    <h1 class="my_red--text text-center mb-4">{{ title }}</h1>
    <v-container class="holer blue--text">
      <v-row wrap>
        <v-col
          style="height: 430px"
          sm="12"
          md="4"
          xl="4"
          align="center"
          v-for="service in services"
          :key="service"
        >
          <Services :card="service" :shadow="shadow" :img_width="img_width" />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import Services from "./Services.vue";
export default {
  components: { Services },
  props: ["title", "services", "shadow", "img_width"],
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
</style>