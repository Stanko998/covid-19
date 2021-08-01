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
      class="px-2"
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

      <v-img :src="logo" max-width="50px" max-height="50px"></v-img>
      <v-spacer />

      <!--<ul>
        <li><NuxtLink to="/" class="link">Home</NuxtLink></li>
        <li><NuxtLink to="/AboutUs" class="link">Services</NuxtLink></li>
        <li><NuxtLink to="/inspire" class="link">Find a doctor</NuxtLink></li>
        <li><NuxtLink to="/Login-Register" class="link">Covid-19</NuxtLink></li>
        <li><NuxtLink to="/" class="link">Contact Us</NuxtLink></li>

        <v-btn id="dugme" color="my_red" rounded>Book Appioment</v-btn>
      </ul>
      -->
      <div class="glavni">
        <v-layout>
          <v-flex v-for="link in links" :key="link">
            <v-btn
              height="100%"
              :color="appBar.color"
              class="font-weight-bold my_red--text rounded-pill mx-1 py-1 px-2"
              active-class=" "
              :to="link.to"
            >
              <span class="my_blue--text"> {{ link.name }}</span>
            </v-btn>
          </v-flex>
        </v-layout>
        <v-btn class="dugme rounded-lg ml-2" color="my_red"
          >Book Appioment</v-btn
        >
      </div>
    </v-app-bar>
    <v-main>
      <div>
        <Nuxt />
      </div>
    </v-main>
    <v-footer absolute app height="250px" id="footer">
      <v-card
        height="100%"
        width="100vw"
        id="holder"
        :color="footer.back_color"
        flat
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
          <v-card-text class="kraj span">
            <v-icon class="margin"> {{ iconica[0] }} </v-icon>+38344222111
          </v-card-text>
          <v-card-text class="kraj span">
            <v-icon class="margin"> {{ iconica[1] }} </v-icon
            >something@gmail.com</v-card-text
          >
          <v-card-text class="kraj span">
            <v-icon class="margin"> {{ iconica[2] }} </v-icon>Somewhere, 12,
            Kosovo</v-card-text
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
    icons: ["mdi-facebook", "mdi-instagram", "mdi-twitter"],
    iconica: ["mdi-phone", "mdi-email", "mdi-map-marker"],
    links: [
      { name: "Home", to: "/" },
      { name: "Services", to: "/inspire" },
      { name: "Find a doctor", to: "/FindADoctor" },
      { name: "Covid-19", to: "/Login-Register" },
      { name: "Contact Us", to: "/AboutUs" },
    ],
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
.v-main {
  background-color: white !important;
}
.v-app-bar {
  .glavni {
    display: flex;
    align-items: center;
    .v-btn {
      box-shadow: none;
      color: white !important;
      text-transform: none;

      &--active {
        color: white !important;
        span {
          color: $red !important;
        }
      }
    }
    .dugme {
      box-shadow: 5px 5px 10px 0px gray;
    }
  }
  /*
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
  }*/
}
#footer {
  background-color: $blue !important;

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
        justify-content: center;
        font-weight: 600;
        font-size: 26px;

        .margin {
          margin-right: 10px;
        }
      }
      .span {
        font-weight: 300;
        font-size: 20px;
      }
    }
  }
}
</style>