<template>
<div>

</div>
</template>

<script>
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
</style>
