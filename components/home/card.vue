<template>
  <div class="card" :style="{ backgroundImage: `url(${src})` }">
    <div class="card-title">
      <span>
        Our <br />
        coffe</span
      >
    </div>
  </div>
</template>

<script>
/**
 * @param {String} title
 * @param {String} src
 * @param {String} color
 * @param {String} link
 */
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    src: {
      type: String,
      required: true,
    },
    color: {
      type: String,
      default: "black",
    },
    link: {
      type: String,
      default: "#",
    },
  },
};
</script>

<style lang="scss" scoped>
.card {
  position: relative;
  height: 230px;
  width: 180px;
  border-radius: 10px;
  //Make image fill the div and cenetr as well
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}

.card-title {
  position: absolute;
  background-color: black;
}
</style>
