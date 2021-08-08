<template>
  <div class="text-center">
    <v-dialog
      v-model="dialog"
      width="500"
      transition="dialog-bottom-transition"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn color="red lighten-2" dark v-bind="attrs" v-on="on">
          Click Me
        </v-btn>
      </template>

      <v-card class="my_blue">
        <v-card-title>
          Appointment
          <v-btn
            class="ml-auto my_red--text my_blue"
            style="box-shadow: none; text-transform: none"
          >
            <v-icon @click="dialog = false"> mdi-close</v-icon>
          </v-btn>
        </v-card-title>

        <v-card-text>
          <v-container>
            <v-row>
              <v-col> <p>Name:</p></v-col>
              <v-col>
                <v-select
                  :items="['0-17', '18-29', '30-54', '54+']"
                  label="Age*"
                ></v-select
              ></v-col>
            </v-row>
            <v-row>
              <v-col> <p>Name:</p></v-col>
              <v-col>
                <v-select
                  :items="['0-17', '18-29', '30-54', '54+']"
                  label="Age*"
                ></v-select>
              </v-col>
            </v-row>
            <v-row>
              <v-col> <p>Name:</p></v-col>
              <v-col> <p>Nesto drugo</p></v-col>
            </v-row>
            <v-row>
              <v-col> <p>Name:</p></v-col>
              <v-col> <p>Nesto drugo</p></v-col>
            </v-row>
            <v-row>
              <v-col> <p>Name:</p></v-col>
              <v-col> <p>Nesto drugo</p></v-col>
            </v-row>
          </v-container>
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="primary" text @click="dialog = false"> I accept </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dialog: false,
    };
  },
};
</script>

<style lang="scss" scoped>
.v-select__slot > .v-label.theme--dark {
  color: orange !important;
}
.v-label.v-label--active.theme--dark.primary--text {
  color: green !important;
}
</style>