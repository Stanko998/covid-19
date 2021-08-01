<template>
  <div>
    <div>
      <v-img :src="img" alt="nema" class="black">
        <div class="centar">
          <h1 class="font-weight-bold mb-6">Why choose us ?</h1>
          <v-container>
            <v-flex row v-for="item in items" :key="item">
              <v-flex
                lg1
                class="display-4 font-weight-bold"
                style="opacity: 0.4"
                >{{ item.id }}</v-flex
              >
              <v-spacer></v-spacer>
              <v-flex lg10>
                <v-flex class="display-1">{{ item.title }}</v-flex>
                <v-flex class="body-1 font-weight-light">
                  <p>
                    {{ item.body }}
                  </p>
                </v-flex>
              </v-flex>
            </v-flex>
          </v-container>
        </div>
      </v-img>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      img: "Images/Home/2.png",
      items: [
        {
          id: 1,
          title: "Expirence",
          body: "Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
        },
        {
          id: 2,
          title: "About Us",
          body: "Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
        },
        {
          id: 3,
          title: "Your",
          body: "Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.display-4,
.display-1,
.body-1 {
  font-family: "Montserrat", sans-serif !important;
}
.centar {
  width: 60%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-top: 20px;
  padding-bottom: 20px;
  padding-left: 5%;
  h1 {
    font-family: "Montserrat", sans-serif !important;
  }
  p {
    width: 80%;
  }
}
.v-btn {
  text-transform: none;
}
</style>