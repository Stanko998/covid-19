<template >
  <div>
    <BestOutcome />
    <OutstandingServices />
  </div>
</template>

<script>
import BestOutcome from "/components/home/BestOutcome.vue";
import OutstandingServices from "../components/home/OutstandingServices.vue";

export default {
  components: { BestOutcome, OutstandingServices },
};
</script>

<style lang="scss" scoped>
</style>
