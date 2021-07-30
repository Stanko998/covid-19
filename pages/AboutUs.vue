<template>
  <div>
    <h1 class="red lighten-4 blue--text text--darken-4">Hello my world</h1>
    <p class="black purple--text text--lighten-2">
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Obcaecati nam
      minima provident laboriosam deserunt culpa quasi dolorem tempora
      laudantium exercitationem, repellat ipsam consequatur dolor veritatis
      tenetur, aut minus voluptates voluptatum soluta saepe architecto adipisci?
      Reprehenderit maiores, tempora explicabo voluptatem voluptates vel
      architecto nam cumque necessitatibus. Sed possimus sit optio repudiandae
      fuga dolore exercitationem! Architecto, quibusdam illo? Illo assumenda et
      debitis dolorum nihil. Harum, iste earum! Quisquam esse nulla iusto, quod
      tempore incidunt eos cumque rerum earum dolore fugiat suscipit itaque ab
      repellendus quaerat magnam nisi vel inventore est adipisci eaque provident
      voluptate! Consequatur neque tenetur saepe, ullam libero veniam, dolor
      ducimus totam aspernatur obcaecati doloremque distinctio rerum.
      Doloremque, consectetur. Placeat neque et numquam a beatae voluptate amet
      voluptatum. Minus iure, enim reprehenderit voluptatibus ex amet quidem
      dolores, itaque fugit omnis fuga voluptate! Molestias exercitationem
      consequuntur laborum quas totam nobis pariatur recusandae porro quis dicta
      non maxime quod sit, cum iusto explicabo neque hic. Magnam quae enim
      impedit sunt, voluptatem soluta cupiditate. Nostrum rem nam aliquam
      doloribus enim possimus iure numquam dolor eligendi cum eveniet quibusdam
      similique laborum quis dicta tempora, sapiente voluptatem molestiae
      asperiores beatae eius, dignissimos itaque? Deleniti incidunt culpa sunt
      natus sapiente, cumque veritatis iste nisi velit labore.
    </p>
    <v-btn class="red lighten-5 grey--text text--darken-3">hi</v-btn>
    <v-btn
      class="blue accent-2 deep-orange--text text--darken-2 font-weight-bold"
      >hi</v-btn
    >
    <v-btn class="rounded-tr-xl">flat button</v-btn>

    <v-btn
      v-for="icon in icons"
      :key="icon"
      class="
        blue
        accent-2
        white--text
        text--darken-2
        font-weight-bold
        mx-2
        px-7
        py-1
        rounded-xl
      "
    >
      <v-icon size="30px" class="d-block">
        {{ icon.tag }}
      </v-icon>
      <v-space class="d-block">{{ icon.name }}</v-space>
    </v-btn>
  </div>
</template>

<script>
export default {
  name: "NuxtAboutus",

  components: {},

  directives: {},

  data() {
    return {
      icons: [
        { tag: "mdi-email", name: "email" },
        { tag: "mdi-youtube", name: "youtube" },
        { tag: "mdi-twitter", name: "twiter" },
        { tag: "mdi-facebook", name: "facebook" },
      ],
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" scoped>
</style>

