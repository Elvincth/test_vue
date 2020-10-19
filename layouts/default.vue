<template>
  <v-app light class="my-app-container">
    <navbar></navbar>
    <homePage></homePage>
  </v-app>
</template>

<script>
import navbar from "@/components/shared/navbar";
import homePage from "@/pages/home";
export default {
  components: {
    navbar,
    homePage,
  },
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
//Set max width
.my-app-container {
  max-width: 1000px;
  margin-left: auto;
  margin-right: auto;
}
</style>
