<template>
  <div>
    <v-img :src="img" alt="nema" class="black">
      <div class="centar">
        <v-layot wrap>
          <v-flex lg4 md5 sm7 xs9>
            <h1 class="font-weight-bold">Best Outcome for Every Patient</h1>
          </v-flex>
          <v-flex md7 sm8>
            <p class="grey--text text--lighten-4 font-weight-light subtitle-1">
              Lorem Ipsum is simply dummy text of the printing and typesetting
              industry. Lorem Ipsum has been the industry's standard dummy text
              ever
            </p>
          </v-flex>
          <v-flex>
            <v-btn
              class="my_red rounded-lg px-3 py-7 font-weight-medium"
              large
              elevation="5"
              >Book Appioment</v-btn
            >
            <BookAppioment info="px-3 py-7 font-weight-medium" />
          </v-flex>
        </v-layot>
      </div>
    </v-img>
  </div>
</template>

<script>
import BookAppioment from "./BookAppioment.vue";
export default {
  components: { BookAppioment },
  data() {
    return {
      img: "Images/Home/1.png",
    };
  },
};
</script>

<style lang="scss" scoped>
.centar {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  background-color: rgba($blue, 34%);
  padding-top: 20px;
  padding-bottom: 20px;
  padding-left: 15%;
  h1 {
    font-family: "Montserrat", sans-serif !important;
  }
  .v-btn {
    text-transform: none;
  }
}
</style>