<template>
  <v-carousel class="mt-10 mb-10" v-bind="settings">
    <!--Loop through images and display it-->
    <v-carousel-item
      v-for="(item, i) in 3"
      :key="i"
      :src="require(`@/assets/images/carousel/${i + 1}.webp`)"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  data() {
    return {
      //Settings for carousel
      settings: {
        height: "350px",
        "show-arrows-on-hover": true,
      },
    };
  },
};
</script>

<style lang="scss" scoped>
::v-deep .v-carousel__controls {
  background-color: transparent;
}

//Dots style
::v-deep .v-carousel__controls__item {
  //On active
  &.v-item--active {
    .mdi-circle {
      color: $carousel-dot-active !important;
    }
  }

  .mdi-circle {
    opacity: 1 !important;
    color: $carousel-dot;
  }
}
</style>
