<template>
  <div id="app">
    <navigationBar />
    <router-view/>

    <div class="container footer">
      <div class="row">


        <div class="col-12 col-sm-6 col-md-3 text-center text-light pt-2 footer-item-1">
          <p class="custom-font">Contact us</p>
          <p>Email: info@thenerdcave.co.za</p>
          <p>Phone: (000) 111 2222</p>
          
        </div>

        <div class="col-12 col-sm-6 col-md-3 text-center text-light pt-2 footer-item-2">
          <p class="custom-font">Location</p>
          <p>6A Street, Al QuozAl Barsha 1</p>
          <p>Dubai, United Arab Emirates</p>
        </div>

        <div class="col-12 col-sm-6 col-md-3 text-center text-light pt-2 footer-item-3">
          <p class="custom-font">Follow us on</p>
          <p> <facebookIcon/> Facebook</p>
        </div>

        <div class="col-12 col-sm-6 col-md-3 text-center text-light pt-2 footer-item-4">
          <p class="custom-font">Secure payments via</p>
          <div class="row">
            <div class="mx-auto">
              <div class="row">
                <img src="@/assets/logos/visaLogo.png" class="img-container mx-1 d-block" alt="">
                <img src="@/assets/logos/mastercardLogo.png" class="img-container mx-1 d-block" alt="">
                <img src="@/assets/logos/instantEftLogo.png" class="img-container mx-1 d-block" alt="">
              </div>
            </div>
          </div>
          <p class="mb-0 custom-font">We ship via</p>
          <img src="@/assets/logos/courierGuy.png" class="img-container mx-auto d-block" alt="">
        </div>
      </div>
    </div>
    <div class="bg-accent container footer p-1">
      <p class="mb-0"> &copy;2020 The Nerd Cave</p>
    </div>
  </div>
</template>

<script>

import navigationBar from '@/components/navigationBar.vue'
import facebookIcon from 'vue-material-design-icons/Facebook.vue'
export default {
  components: {
    navigationBar,
    facebookIcon
  }
}
</script>

<style>
</style>
