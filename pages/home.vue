<template>
  <div class="mb-10">
    <!--Hero banner-->
    <hero></hero>
    <!--Carousel banner-->
    <carousel></carousel>
    <!--Card-->
    <div class="ml-5 mr-5 d-flex justify-center" style="width: 100%">
      <div class="card-wrapper" v-for="(item, i) in cardItems" :key="i">
        <card
          :title="item.title"
          :rgbColor="item.rgbColor"
          :src="item.src"
        ></card>
      </div>
    </div>

    <!--FAB Button-->
    <v-btn color="pink" dark small absolute bottom left fab
      ><v-icon>home</v-icon></v-btn
    >
  </div>
</template>

<script>
import hero from "@/components/home/hero";
import carousel from "@/components/home/carousel";
import card from "@/components/home/card";
export default {
  components: {
    hero,
    carousel,
  },
  data() {
    return {
      cardItems: [
        {
          title: "our coffee",
          rgbColor: "0,0,0",
          src: require("@/assets/images/card/coffee.jpg"),
        },
        {
          title: "our pastry",
          rgbColor: "214,185,68",
          src: require("@/assets/images/card/pastry.jpg"),
        },
        {
          title: "our food",
          rgbColor: "93,122,89",
          src: require("@/assets/images/card/food.jpg"),
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.card-wrapper {
  margin-right: 5rem;
}
</style>

