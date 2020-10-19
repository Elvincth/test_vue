<template>
  <div class="my-card-container" :style="cssVars">
    <div class="card" :style="{ backgroundImage: `url(${src})` }"></div>
    <div class="card-title">
      <span>{{ title }}</span>
    </div>
    <div></div>
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
    rgbColor: {
      type: String,
    },
    link: {
      type: String,
      default: "#",
    },
  },
  computed: {
    cssVars() {
      return {
        "--rgbColor": this.rgbColor,
      };
    },
  },
};
</script>

<style lang="scss" scoped>
$radius: 10px;
$height: 230px;
$width: 180px;

@mixin card {
  height: $height;
  width: $width;
  border-radius: $radius;
  //Make image fill the div and cenetr as well
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}

.my-card-container {
  position: relative;
  height: $height;
  width: $width;
}

.card {
  @include card;
  position: relative;
  overflow: hidden;

  &::before {
    transition: transform 0.2s;
    content: " ";
    position: absolute;
    background-image: inherit;
    @include card;
  }

  &:hover::before {
    transform: scale(1.3);
  }
}

.my-card-container:hover .card-title {
  transform: scale(1.9) translate(-21px, -29px);
  backdrop-filter: blur(5px);
  background-color: rgba(var(--rgbColor), 0.6);
}

.card-title {
  position: absolute;
  background-color: rgba(var(--rgbColor), 1);
  height: calc(#{$height} / 1.8);
  width: calc(#{$width} / 1.8);
  transition: all 0.2s ease-in-out;
  text-transform: capitalize; //Make all captialize
  font-size: 1.6rem;
  border-radius: $radius;
  transform: translate(15px, 15px); //move it down
  bottom: 0;
  right: 0;
  padding: 0.7rem;
  display: flex;
  span {
    margin-top: auto;
    padding-bottom: 5px; //make it fit
    white-space: pre-line; //All word in new line
    color: #fff;
    font-weight: bold;
  }
}
</style>
