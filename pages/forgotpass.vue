<template>
    <div class="h-screen flex">
      <div class="w-2/5 px-[80px] py-[80px]">
        <LogibugLogo />
        <forgot-title/>
        <forgot-form />
      </div>
      <div class="w-3/5 bg-blue-500">
      <img src="../components/assets/FrameForm.svg" alt="Image" class="object-cover w-full h-full">

      </div>
    </div>
  </template>
  
  <script>
  
  import ForgotTitle from '../components/Forgot/ForgotTitle.vue';
  import ForgotForm from '../components/Forgot/ForgotForm.vue';
  import LogibugLogo from '../components/major/LogibugLogo.vue';
  
  export default {
    components: {
      LogibugLogo,
      ForgotTitle,
      ForgotForm,
    }
  }
  </script>
  
  <style >
  .h-screen {
    min-height: 100vh;
  }
  
  .bg-blue-500 {
    height: 100%;
  }
  </style>