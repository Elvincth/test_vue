<template>
  <div class="d-flex ml-2 mr-2 mt-5 align-center nav-bar">
    <img class="logo" src="~/assets/images/logo.jpg" />
    <div class="items ml-auto">
      <a href="#">About</a>
      <a href="#">Promotion</a>
      <a href="#">Shop</a>
      <a href="#">Our Store</a>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
//Set max width
.my-app-container {
  max-width: 1000px;
  margin-left: auto;
  margin-right: auto;
}

//For nav bar
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
</style>
