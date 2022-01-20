<template>
  <div>
    <div class="task">
      <h1>{{ task.title }}</h1>
    </div>
  </div>
</template>

<script>
export default {
  props: ["task"],
};
</script>

<style lang="scss" scoped>
.task {
  background-color: rgba(0, 0, 0, 0.35);
  h1 {
    color: green !important;
  }
}
</style>