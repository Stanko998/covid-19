<template>
  <v-app light>
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
        <li><NuxtLink to="/" class="link">Services</NuxtLink></li>
        <li><NuxtLink to="/" class="link">Find a doctor</NuxtLink></li>
        <li><NuxtLink to="/" class="link">Covid-19</NuxtLink></li>
        <li><NuxtLink to="/" class="link">Contact Us</NuxtLink></li>
        <v-btn id="dugme" color="my_red" rounded>Book Appioment</v-btn>
      </ul>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer app> </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      logo: "/logo.png",
      appBar: {
        color: "#ffffff",
      },
    };
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

/*}*/
</style>