<template>
    <div class="pt-[90px] pl-[90px] justify-center items-center min-h-screen bg-[#EDF1FF]">
      <div class="container grid grid-cols-4 pl">
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
  import SosialMedia from '../footer/SosialMedia.vue';
  import CompanyFooter from '../footer/CompanyFooter.vue';
  import ServiceFooter from '../footer/ServiceFooter.vue';
  import ContactFooter from '../footer/ContactFooter.vue';
  import MainFooter from '../footer/MainFooter.vue';
  
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
  