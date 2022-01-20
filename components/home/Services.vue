<template>
  <div style="height: 100%">
    <v-card
      style="height: 100%"
      color="white"
      class="rounded-lg my_blue--text pa-3 mx-md-8"
      :class="shadow"
    >
      <v-img :src="card.img" :width="img_width" class="rounded-0"> </v-img>
      <h2 class="mb-5 1 font-weight-bold headline">
        {{ card.title }}
      </h2>
      <p class="caption">{{ card.body }}</p>
    </v-card>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: ["card", "shadow", "img_width"],
  mounted() {},
  methods: {},
};
</script>

<style lang="scss" scoped>
@media (max-width: "681px") {
  .v-card {
    h2 {
      width: 100% !important;
    }
  }
}
.v-card {
  transition: 400ms;
  box-shadow: none !important;
  &:hover {
    box-shadow: 5px 5px 10px 0px grey !important;
  }
  .caption {
    font-family: "Montserrat", sans-serif !important;
  }
  h2 {
    width: 80%;
    font-family: "Montserrat", sans-serif !important;
  }
  p {
    text-align: center;
  }
}
.shadow {
  box-shadow: 5px 5px 10px 0px grey !important;
}
</style>