<template>
  <v-app dark>
    <!-- 
      <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    -->
    <v-app-bar
      id="nav-bar"
      :color="appBar.color"
      min-width="100vw"
      fixed
      app
      hide-on-scroll
    >
      <!-- <v-app-bar-nav-icon @click.stop="drawer = !drawer" /> 
    
      <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon>mdi-{{ `chevron-${miniVariant ? "right" : "left"}` }}</v-icon>
      </v-btn>
      <v-btn icon @click.stop="clipped = !clipped">
        <v-icon>mdi-application</v-icon>
      </v-btn>
      <v-btn icon @click.stop="fixed = !fixed">
        <v-icon>mdi-minus</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      -->

      <v-img
        :src="logo"
        max-width="50px"
        max-height="50px"
        margin="30px"
      ></v-img>
      <v-spacer />
      <ul>
        <li><NuxtLink to="/" class="link">Home</NuxtLink></li>
        <li><NuxtLink to="/AboutUs" class="link">Services</NuxtLink></li>
        <li><NuxtLink to="/inspire" class="link">Find a doctor</NuxtLink></li>
        <li><NuxtLink to="/Login-Register" class="link">Covid-19</NuxtLink></li>
        <li><NuxtLink to="/" class="link">Contact Us</NuxtLink></li>

        <v-btn id="dugme" color="my_red" rounded>Book Appioment</v-btn>
      </ul>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer absolute app height="250px">
      <v-card
        height="100%"
        width="100vw"
        id="holder"
        :color="footer.back_color"
      >
        <v-card flat :color="footer.back_color" class="placer">
          <v-card-text class="kraj">Our Name</v-card-text>
          <v-card-text class="kraj icon">
            <v-btn
              width="10px"
              height="15px"
              v-for="icon in icons"
              :key="icon"
              class="mx-4"
              icon
            >
              <v-icon size="30px">
                {{ icon }}
              </v-icon>
            </v-btn>
          </v-card-text>
        </v-card>
        <v-card flat :color="footer.back_color" class="placer right">
          <v-card-text class="kraj">Contact</v-card-text>
          <v-card-text class="kraj">
            <v-icon class="magin"> {{ iconica[0] }} </v-icon>+381 4854 84 21
          </v-card-text>
          <v-card-text class="kraj">
            <v-icon class="magin"> {{ iconica[1] }} </v-icon
            >kdmsaifa@gmail.com</v-card-text
          >
          <v-card-text class="kraj">
            <v-icon class="magin"> {{ iconica[2] }} </v-icon>lole
            cigana.12</v-card-text
          >
        </v-card>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    logo: "/logo.png",
    appBar: {
      color: "#ffffff",
    },
    footer: {
      back_color: "my_blue",
    },
    icons: ["mdi-facebook", "mdi-instagram", "mdi-google"],
    iconica: ["mdi-phone", "mdi-email", "mdi-map-marker"],
    padless: false,
    variant: "default",
  }),
  computed: {
    localAttrs() {
      const attrs = {};

      if (this.variant === "default") {
        attrs.absolute = false;
        attrs.fixed = false;
      } else {
        attrs[this.variant] = true;
      }
      return attrs;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "assets/variables";
#nav-bar {
  ul {
    display: flex;
    align-items: center;
    margin-right: 20px;
    li {
      list-style: none;
      margin-right: 15px;
      .link {
        color: $blue;
        text-decoration: none;
        font-weight: 700;
        transition: 300ms;
        border-radius: 10px;
        padding: 4px 10px;
        &:hover {
          background-color: $red;
          color: white;
        }
      }
    }
    #dugme {
      box-shadow: 5px 5px 15px 0px black;
    }
  }
}
#holder {
  display: flex;
  align-items: center;
  justify-content: space-around;
  .placer {
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    .kraj {
      font-weight: 500;
      font-size: 22px;
      height: 45px;
      width: 100%;
      color: #fff;
      padding: 5px;
      margin: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }
    .icon {
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: row;
      > * {
        margin: 5px;
        padding: 0;
      }
    }
  }
  .right {
    .kraj {
      align-items: flex-start;
      display: inline-block;
      .magin {
        margin-right: 10px;
      }
    }
  }
}
/*}*/
</style>