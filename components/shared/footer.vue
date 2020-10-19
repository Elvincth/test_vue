<template>
  <footer class="footer-container">
    <div class="my-wrapper d-flex mt-13">
      <div class="d-flex flex-column">
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
      </div>

      <div></div>
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
</style>
