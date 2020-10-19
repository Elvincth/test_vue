<template>
  <div>
    <!--Hero banner-->
    <hero></hero>
    <!--Carousel banner-->
    <carousel></carousel>
    <!--Card-->
    <card title="Our coffee" src="xxx"></card>
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

