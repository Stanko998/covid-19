<template >
  <div>
    <BestOutcome />
    <Outstanding
      :title="Outsandings[0].title"
      :services="Outsandings[0].services"
      :shadow="Outsandings[0].shadow"
      :img_width="Outsandings[0].img_width"
    />
    <WhyUs />
    <Outstanding
      :title="Outsandings[1].title"
      :services="Outsandings[1].services"
      :shadow="Outsandings[1].shadow"
      :img_width="Outsandings[1].img_width"
    />
  </div>
</template>

<script>
import BestOutcome from "/components/home/BestOutcome.vue";
import Outstanding from "../components/home/Outstanding.vue";
import WhyUs from "../components/home/WhyUs.vue";

export default {
  components: { BestOutcome, Outstanding, WhyUs },
  data() {
    return {
      Outsandings: [
        {
          title: "Our Outstanding Services",
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
          shadow: "noshadow",
          img_width: "150px",
        },
        {
          title: "Outstanding Departmental",
          services: [
            {
              img: "Images/Home/Cardilogy.png",
              title: "Cardilogy",
              body: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. ",
            },
            {
              img: "Images/Home/Neurology.png",
              title: "Neurology",
              body: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. ",
            },
            {
              img: "Images/Home/Dental.png",
              title: "Dental",
              body: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. ",
            },
          ],
          shadow: "shadow",
          img_width: "336px",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
</style>
