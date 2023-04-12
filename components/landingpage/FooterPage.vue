<template>
  <div class="py-[70px] items-center bg-[#EDF1FF] font-montserrat">
    <div class="flex justify-around">
      <SosialMedia />
      <CompanyFooter />
      <ServiceFooter />
      <ContactFooter />
    </div>
    <div class="flex justify-center mt-[70px]">
      <MainFooter />
    </div>
  </div>
</template>
  
<script>
import SosialMedia from '../footer/SosialMedia.vue';
import CompanyFooter from '../footer/CompanyFooter.vue';
import ServiceFooter from '../footer/ServiceFooter.vue';
import ContactFooter from '../footer/ContactFooter.vue';
import MainFooter from '../footer/MainFooter.vue';

export default {
  components: {
    SosialMedia,
    CompanyFooter,
    ServiceFooter,
    ContactFooter,
    MainFooter
  }
}
</script>
  
<style ></style>+