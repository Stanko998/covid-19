<template>
  <v-app>
    <!-- 
      <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app>
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
    <v-app-bar class="px-2" fixed app hide-on-scroll color="white">
      <v-toolbar flat color="white">
        <v-toolbar-title>
          <v-img :src="logo" max-width="50px" max-height="50px"></v-img>
        </v-toolbar-title>
        <v-spacer />
        <v-toolbar-items class="glavni">
          <v-layout align-center>
            <v-flex v-for="link in links" :key="link">
              <v-btn
                height="100%"
                class="font-weight-bold rounded-pill mx-1 py-1 px-2 white"
                :to="link.to"
              >
                <span class="my_blue--text"> {{ link.name }} </span>
              </v-btn>
            </v-flex>
            <BookAppioment />
          </v-layout>
        </v-toolbar-items>
      </v-toolbar>
    </v-app-bar>

    <v-main class="white">
      <div>
        <Nuxt />
      </div>
    </v-main>

    <v-footer absolute app height="250px" class="my_blue">
      <v-card height="100%" width="100vw" id="holder" class="my_blue" flat>
        <v-card flat class="placer my_blue">
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
        <v-card flat class="placer right my_blue">
          <v-card-text class="kraj">Contact</v-card-text>
          <v-card-text
            class="kraj span"
            v-for="contact in Contacts"
            :key="contact"
          >
            <v-icon class="margin"> {{ contact.icon }} </v-icon
            >{{ contact.body }}
          </v-card-text>
        </v-card>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
import BookAppioment from "../components/home/BookAppioment.vue";
export default {
  components: { BookAppioment },
  data: () => ({
    logo: "/logo.png",
    icons: ["mdi-facebook", "mdi-instagram", "mdi-twitter"],
    Contacts: [
      {
        icon: "mdi-phone",
        body: "+38344222111",
      },
      {
        icon: "mdi-email",
        body: "something@gmail.com",
      },
      {
        icon: "mdi-map-marker",
        body: "Somewhere, 12, Kosovo",
      },
    ],
    links: [
      { name: "Home", to: "/" },
      { name: "Services", to: "/Services" },
      { name: "Find a doctor", to: "/FindADoctor" },
      { name: "Covid-19", to: "/Covid-19" },
      { name: "Contact Us", to: "/ContactUs" },
    ],
  }),
};
</script>

<style lang="scss" scoped>
@import "assets/variables";

.v-app-bar .v-toolbar__items {
  .v-btn {
    box-shadow: none;
    text-transform: none;
    &--active span {
      color: $red !important;
    }
  }
  .dugme {
    box-shadow: 5px 5px 10px 0px gray;
  }
}

.v-footer #holder {
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
</style>