<template>
  <div>
    <v-img :src="img" height="500px">
      <v-layout
        style="height: 100%"
        wrap
        class="py-16 px-5"
        justify-space-around
        align-content-space-around
      >
        <v-flex
          sm5
          class="text-center"
          v-for="infocard in infocards"
          :key="infocard"
        >
          <InfoCard :infocard="infocard" />
        </v-flex>
      </v-layout>
    </v-img>
  </div>
</template>

<script>
import InfoCard from "./InfoCard.vue";
export default {
  components: { InfoCard },
  data() {
    return {
      img: "Images/Covid-19/1.png",
      infocards: [
        {
          icon: "mdi-phone",
          color: "red darken-4",
          span: "19 920",
          body: "Suport for the elderly",
        },
        {
          icon: "mdi-file-document",
          color: "green",
          span: "",
          body: "check your medical symtoms",
        },
        {
          icon: "mdi-phone",
          color: "red darken-4",
          span: "19 819",
          body: "Information Line For all question about covid-19",
        },
        {
          icon: "mdi-whatsapp",
          color: "deep-purple lighten-1",
          span: "",
          body: "Covid-19 info",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
</style>