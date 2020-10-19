<template>
  <v-app light>
    <div class="my-app-container">
      <navbar></navbar>
      <!--Actually we need a router outlet here but since it is a SPA,
    so I made just a single component as page-->
      <homePage></homePage>
    </div>
    <!--Footer for all-->
    <myFooter></myFooter>
  </v-app>
</template>

<script>
import navbar from "@/components/shared/navbar";
import homePage from "@/pages/home";
import myFooter from "@/components/shared/footer";

export default {
  components: {
    navbar,
    homePage,
    myFooter,
  },
  data() {
    return {};
  },
};
</script>

<style>
:root {
  --main: #f1d04b;
}
</style>

<style lang="scss" scoped>
//Set max width
.my-app-container {
  max-width: 1000px;
  margin-left: auto;
  margin-right: auto;
}
</style>
