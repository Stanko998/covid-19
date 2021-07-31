<template >
  <v-layout class="blue" wrap row justify-center>
    <v-flex class="red" xs6>
      <h1>text</h1>
    </v-flex>
    <v-flex xs6>
      <v-flex class="green" xs12>
        <h1>text</h1>
      </v-flex>
      <v-flex xs6>
        <v-spacer></v-spacer>
      </v-flex>
    </v-flex>
    <v-flex class="red" xs4>
      <h1>text</h1>
    </v-flex>
  </v-layout>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
h1 {
  color: black;
}
</style>
