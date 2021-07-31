<template>
  <div>
    <v-card color="white" class="rounded-lg my_blue--text pa-3">
      <v-img :src="card.img" width="150px"> </v-img>
      <h2 class="mb-5">{{ card.title }}</h2>
      <p class="caption">{{ card.body }}</p>
    </v-card>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: ["card"],
};
</script>

<style lang="scss" scoped>
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
  }
}
</style>