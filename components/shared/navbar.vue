<template>
  <div>
    <div class="desktop-only">
      <div class="d-flex ml-2 mr-2 mt-5 align-center nav-bar">
        <img class="logo" src="~/assets/images/logo.jpg" />
        <div class="items ml-auto">
          <a v-for="(item, i) in items" :key="i" :href="item.href">{{
            item.name
          }}</a>
        </div>
      </div>
    </div>

    <!--For mobile-->
    <div class="mobile-only">
      <v-app-bar color="dark" dark>
        <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
        <v-toolbar-title>Lassana</v-toolbar-title>
      </v-app-bar>

      <v-navigation-drawer v-model="drawer" absolute temporary>
        <v-list nav dense>
          <v-list-item-group v-model="group" active-class="text--accent-4">
            <v-list-item
              v-for="(item, i) in items"
              :key="i"
              :href="item.href"
              link
            >
              <v-list-item-title>{{ item.name }}</v-list-item-title>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      group: null,
      items: [
        {
          name: "About",
          href: "#",
        },
        {
          name: "Promotion",
          href: "#",
        },
        {
          name: "Shop",
          href: "#",
        },
        {
          name: "Our Store",
          href: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
//Set max width
.my-app-container {
  max-width: 1000px;
  margin-left: auto;
  margin-right: auto;
}

//For nav bar
.desktop-only {
  .nav-bar {
    .logo {
      width: 3rem;
    }
    //Nav items
    .items {
      a {
        font-weight: 500;
        color: $font-color;
        margin-left: 3rem;
        text-decoration: none;
      }
    }
  }
}

.mobile-only {
  display: none;
}

@media (max-width: 575px) {
  .desktop-only {
    display: none;
  }

  .mobile-only {
    display: block !important;
  }
}
</style>
