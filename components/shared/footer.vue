<template>
  <footer class="footer-container d-flex flex-column">
    <!--Contact Section-->
    <div
      class="my-wrapper justify-space-between d-flex flex-wrap mt-13 ml-5 mr-5"
    >
      <div class="d-inline-flex flex-column">
        <span
          style="font-size: 1.2rem"
          class="text-capitalize font-weight-bold"
        >
          want to know lassaana better?
        </span>

        <!--Social Media Section-->
        <div class="mt-3">
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
          <span>custom service: <a class="tel">63930906</a></span>
        </div>
      </div>

      <!--Logo section-->
      <div>
        <v-img
          cover
          width="100"
          :src="require('@/assets/images/logo.png')"
        ></v-img>
      </div>
    </div>

    <div class="copyright-container mb-5">
      <span> © 2015 by LASSANA Limited </span>
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
.copyright-container {
  width: 100%;
  color: white;
  font-size: 0.95rem;
  text-align: center;
  font-weight: bold;
  margin-top: auto;
}

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
    width: 100%;
    margin-left: auto !important;
    margin-right: auto !important;
    color: white;
  }
}

// @media (max-width: 300px){
//       //contact
//     .contact-container{flex-direction: column!important;
//     }
// }
</style>
