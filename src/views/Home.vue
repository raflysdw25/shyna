<template>
  <div class="home">
    <!-- Header -->
    <HeaderShyna/>

    <!-- Carousel (Hero Section) -->
    <HeroShyna/>

    <!-- Women Banner -->
    <WomenBannerShyna/>

    <!-- InstaShyna -->
    <InstaShyna/>

    <!-- Partner Logo -->
    <PartnerLogoShyna/>

    <!-- Footer -->
    <FooterShyna/>
  </div>
</template>



<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderShyna from '@/components/HeaderShyna.vue';
import HeroShyna from '@/components/HeroShyna.vue';
import WomenBannerShyna from '@/components/WomenBannerShyna.vue';
import InstaShyna from '@/components/InstaShyna.vue';
import PartnerLogoShyna from '@/components/PartnerLogoShyna.vue';
import FooterShyna from '@/components/FooterShyna.vue';



export default {
  name: 'Home',
  components: {
    HeaderShyna,
    HeroShyna,
    WomenBannerShyna,
    InstaShyna,
    PartnerLogoShyna,
    FooterShyna
  }
}
</script>
