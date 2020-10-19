<template>
  <div class="mb-10">
    <!--Hero banner-->
    <hero></hero>
    <!--Carousel banner-->
    <carousel></carousel>
    <!--Card-->
    <div class="ml-5 mr-5">
      <card
        title="Our coffee"
        :src="require('@/assets/images/card/coffee.jpg')"
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
};
</script>

