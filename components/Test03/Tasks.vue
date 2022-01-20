<template>
  <div>
    <Task v-for="task in tasks" :key="task.id" :task="task" />
  </div>
</template>

<script>
import Task from "./Task.vue";

export default {
  components: { Task },
  data() {
    return {
      tasks: [
        {
          id: 1,
          title: "Ponedelja",
          time: "12.5.2021 12:20",
          recomended: true,
        },
        {
          id: 2,
          title: "Utorak",
          time: "12.5.2021 12:20",
          recomended: true,
        },
        {
          id: 3,
          title: "Sreda",
          time: "12.5.2021 12:20",
          recomended: true,
        },
        {
          id: 4,
          title: "cetvratk",
          time: "12.5.2021 12:20",
          recomended: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
</style>
