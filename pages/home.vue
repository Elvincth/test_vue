<template>
  <div class="d-flex flex-wrap hero-container ml-2 mr-2 mt-6">
    <!--Hero text-->
    <div>
      <h1>Lassana Delights Your Daily Coffee Experience</h1>
      <p>
        Lassana is a Hong Kong local brand that specialize in coffee and fresh
        bakery. We are here to provide excellent food excellent food service
        that inspire you everyday.
      </p>
    </div>
    <!--Hero Image-->
    <div>
      <v-img class="ml-auto mr-auto" contain :src="require('@/assets/images/hero-image.jpg')"></v-img>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
};
</script>

<style lang="scss" scoped>
.hero-container {
  div {
    width: 50%;
  }
}
</style>
