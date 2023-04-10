<template>
    <div class="min-h-screen w-screen flex flex-col justify-center items-center font-['Monserrat'] overflow-hidden gap-x-2">
      <text-page ></text-page>
      <div class="flex  flex-col md:flex-row justify-center items-center space-y-8 md:space-y-0 md:gap-x-40 md:justify-center">
        <div class="flex justify-between items-center gap-x-10">
          <div >
            <img src="../assets/ContentImage4.svg" alt="images" class="object-cover w-full h-[400px]">
            <image-content></image-content>
            <register-button></register-button>
          </div>
        </div>
        <div class="justify-between items-center gap-x-10">
          <div >
            <img src="../assets/ContentImage5.svg" alt="images" class="object-cover w-full h-[400px]">
            <download-content></download-content>
            <download-button></download-button>
          </div>
        </div>
      </div>
    </div>
  </template>

  
  <script>
  import ImageContent from '../download/ImageContent.vue';
  import TextPage from './TextPage.vue';
  import RegisterButton from '../download/RegisterButton.vue';
  import DownloadButton from '../download/DownloadButton.vue';
  import DownloadContent from '../download/DownloadContent.vue';
  
  
  export default {
    components: {
      ImageContent,
      TextPage,
      RegisterButton,
      DownloadButton,
      DownloadContent
    }
  }
  </script>
  
  <style>
  html,body{
    margin: 0;
    height: 100%;

  }
 
  </style>
  