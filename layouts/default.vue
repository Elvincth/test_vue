<template>
  <v-app light class="my-app-container ">
    <div class="d-flex align-center nav-bar ">
      <img class="logo" src="~/assets/images/logo.jpg" />
      <div class="items ml-auto">
        <a>About</a>
        <a>Promotion</a>
        <a>Shop</a>
        <a>Our Store</a>
      </div>
    </div>
  </v-app>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
//For nav bar
.nav-bar {
  .logo {
    width: 3rem;
  }
  //Nav items
  .items {
    a {
      color: $font-color;
      margin-left: 3rem;
    }
  }
}
</style>
