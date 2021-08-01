<template>
  <div>
    <Dropdown />
    <Outstanding
      :title="Outsandings[0].title"
      :services="Outsandings[0].services"
      :shadow="Outsandings[0].shadow"
      :img_width="Outsandings[0].img_width"
    />
  </div>
</template>

<script>
import Dropdown from "../components/FindADoctor/Dropdown.vue";
import Outstanding from "../components/home/Outstanding.vue";
export default {
  components: { Outstanding, Dropdown },

  directives: {},

  data() {
    return {
      Outsandings: [
        {
          title: "",
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
          img_width: "340px",
        },
      ],
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" scoped>
</style>