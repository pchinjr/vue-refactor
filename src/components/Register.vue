<template>
  <div>
    <RegisterProduct :serial="serial"/>
    <PromoCode/>
  </div>
</template>
<script>
/*import Kickstarter from './Kickstarter.vue'
import Navigation from './Navigation.vue'
import BannerImage from './BannerImage.vue'*/
import RegisterProduct from './RegisterProduct.vue'
import PromoCode from './PromoCode.vue'
export default {
  name: 'Register',
  components: {
    /*Kickstarter,
    Navigation,
    BannerImage,*/
    RegisterProduct,
    PromoCode
  },
  computed:{
    serial: function(){
      return this.$route.query.productId
    }
  }
}
</script>
