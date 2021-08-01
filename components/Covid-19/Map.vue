<template>
  <div>
    <v-layout align-center>
      <v-container class="pl-5">
        <v-row
          align-content="center"
          justify="center"
          v-for="legend in legends"
          :key="legend"
        >
          <v-col
            cols="3"
            align-self="center"
            :class="legend.color"
            style="height: 50px"
          >
          </v-col>
          <v-col cols="8" align-self="center black--text font-weight-light">
            {{ legend.body }} cases
          </v-col>
        </v-row>
      </v-container>
      <Svet class="mr-6" />
    </v-layout>
  </div>
</template>

<script>
import Svet from "./Svet.vue";
export default {
  components: { Svet },
  data() {
    return {
      legends: [
        {
          color: "grey",
          body: "No registered",
        },
        {
          color: "blue lighten-5",
          body: "0 - 10 000 ",
        },
        {
          color: "blue lighten-3",
          body: "10 101 - 50 000",
        },
        {
          color: "blue lighten-1",
          body: "50 001 - 100 000",
        },
        {
          color: "blue darken-1",
          body: "100 001 - 500 000",
        },
        {
          color: "blue darken-3",
          body: "500 001 - 1 000 000",
        },
        {
          color: "red lighten-1",
          body: "1 000 001 - 5 000 000",
        },
        {
          color: "red darken-2",
          body: "5 000 001-10 000 000",
        },
        {
          color: "red darken-4",
          body: ">10 000 000",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
</style>