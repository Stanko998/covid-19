<template>
  <div class="py-5">
    <h1 class="my_red--text text-center mb-4">Our Outstanding Services</h1>
    <v-container class="holer blue--text">
      <v-row justify="space-around">
        <v-col
          sm="4"
          md="3"
          xl="3"
          align="center"
          v-for="service in services"
          :key="service"
        >
          <Services :card="service" />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import Services from "./Services.vue";
export default {
  components: { Services },
  data() {
    return {
      services: [
        {
          img: "Images/Home/Health Checkups.png",
          title: "Health Checkups",
          body: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever. Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
        },
        {
          img: "Images/Home/Emergency Ambulance.png",
          title: "Emergency Ambulance",
          body: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever. Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
        },
        {
          img: "Images/Home/247 Special Services.png",
          title: "247 Special Services",
          body: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever. Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
</style>