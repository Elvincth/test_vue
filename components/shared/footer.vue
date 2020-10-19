<template>
  <footer class="footer-container">

    <!--Contact Section-->
    <div
      class="my-wrapper d-flex flex-wrap justify-space-between mt-13 ml-5 mr-5"
    >
      <div class="d-flex flex-column" style="width: 100%">
        <p style="font-size: 1.2rem" class="text-capitalize font-weight-bold">
          want to know lassaana better?
        </p>

        <!--Social Media Section-->
        <div>
          <a aria-label="Facebook" href="https://facebook.com" class="mr-2">
            <span class="fb-logo material-icons"> facebook </span>
          </a>

          <!--Added aria label for accessibility -->
          <a aria-label="Instagram" href="https://instagram.com">
            <instagramIcon></instagramIcon>
          </a>
        </div>

        <!--Contact section-->
        <div class="text-capitalize font-weight-bold mt-3">
          <p>custom service: <a class="tel">63930906</a></p>
        </div>
      </div>

      <!--Logo section-->
      <div class="ml-auto">
        <v-img
          class="ml-auto mr-auto"
          cover
          width="100"
          :src="require('@/assets/images/logo.png')"
        ></v-img>
      </div>
    </div>
  </footer>
</template>

<script>
import instagramIcon from "@/components/svg/instagram";
export default {
  components: { instagramIcon },
};
</script>

<style lang="scss" scoped>
.fb-logo {
  color: white;
  font-size: 39.5px;
}

.tel {
  color: white;
}

.footer-container {
  background: black;
  min-height: 300px;
  width: 100%;

  .my-wrapper {
    max-width: 1000px;
    margin-left: auto;
    margin-right: auto;
    color: white;
  }
}

// @media (max-width: 300px){
//       //contact
//     .contact-container{flex-direction: column!important;
//     }
// }
</style>
