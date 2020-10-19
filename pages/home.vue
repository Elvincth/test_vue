<template>
  <div class="mb-10">
    <!--Hero banner-->
    <hero></hero>
    <!--Carousel banner-->
    <carousel></carousel>
    <!--Card-->
    <div class="ml-5 mr-5">
      <card
        v-for="(item, i) in cardItems"
        :key="i"
        :title="item.title"
        :rgbColor="item.rgbColor"
        :src="item.src"
      ></card>
    </div>
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
          rgbColor: "0,0,0",
          src: require("@/assets/images/card/pastry.jpg"),
        },
        {
          title: "our food",
          rgbColor: "0,0,0",
          src: require("@/assets/images/card/food.jpg"),
        },
      ],
    };
  },
};
</script>

