<template>
  <div class="mb-10">
    <!--Hero banner-->
    <hero></hero>
    <!--Carousel banner-->
    <carousel></carousel>
    <!--Card-->
    <div
      class="d-flex flex-wrap justify-content-center align-center"
      style="width: 100%"
    >
      <div
        class="card-wrapper ml-auto mr-auto"
        v-for="(item, i) in cardItems"
        :key="i"
      >
        <card
          :title="item.title"
          :rgbColor="item.rgbColor"
          :src="item.src"
        ></card>
      </div>
    </div>

    <!--FAB Button-->
    <v-btn color="var(--main)" light fixed bottom right fab
      ><span class="material-icons">shopping_basket</span>
    </v-btn>

    <!--Sub footer-->
    <div class="d-flex flex-wrap flex-column mt-15 ml-3 mr-3">
      <div>
        <p class="font-weight-bold">
          For Further Information About Lassana Service including Coffee and
          Fresh Bakery
        </p>
      </div>
      <div>
        <v-btn elevation="0" large color="var(--main)"
          ><span style="color: white">Contact Us</span></v-btn
        >
      </div>
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
.card-wrapper:not(:last-child) {
  margin-right: 5rem;
}
.card-wrapper {
  height: 280px;
  width: 200px;
}
</style>

