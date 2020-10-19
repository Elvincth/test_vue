<template>
  <div class="d-flex flex-wrap hero-container ml-2 mr-2 mt-10">
    <!--Hero text-->
    <div class="d-flex flex-column align-center">
      <h1>Lassana Delights Your Daily Coffee Experience</h1>
      <p class="mt-5">
        Lassana is a Hong Kong local brand that specialize in coffee and fresh
        bakery. We are here to provide excellent food excellent food service
        that inspire you everyday.
      </p>
    </div>
    <!--Hero Image-->
    <div>
      <v-img
        class="ml-auto mr-auto"
        cover
        aspect-ratio="1"
        width="350"
        :src="require('@/assets/images/hero-image.jpg')"
      ></v-img>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.hero-container {
  div {
    width: 50%;
  }
}

@media (max-width: 575.98px) {
  .hero-container {
    div {
      width: 100% !important;
      ::v-deep .v-image {
        max-width: 250px;
      }
    }
  }
}
</style>
