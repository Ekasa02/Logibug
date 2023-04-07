<template>
    <div class="pt-[90px] justify-center items-center min-h-screen bg-[#EDF1FF]">
      <div class="container grid grid-cols-4 ">
        <div>
          <sosial-media></sosial-media>
        </div>
        <div>
          <company-footer></company-footer>
        </div>
        <div>
          <service-footer></service-footer>
        </div>
        <div>
          <contact-footer></contact-footer>
        </div>
      </div>
      <div style="display: flex; justify-content: center; padding-top:150px">
        <main-footer></main-footer>
      </div>
    </div>
    
   
  </template>
  
  <script>
  import SosialMedia from '../components/footer/SosialMedia.vue';
  import CompanyFooter from '../components/footer/CompanyFooter.vue';
  import ServiceFooter from '../components/footer/ServiceFooter.vue';
  import ContactFooter from '../components/footer/ContactFooter.vue';
  import MainFooter from '../components/footer/MainFooter.vue';
  
  export default {
    components:{
      SosialMedia,
      CompanyFooter,
      ServiceFooter,
      ContactFooter,
      MainFooter
    }
  }
  </script>
  
  <style >
  .grid {
    display: grid;
    grid-gap: 6rem;
  }

  .content{
     margin-bottom: 8rem;
  }
  
  
  </style>
  