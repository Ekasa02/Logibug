<template>
    <div class="h-screen flex">
      <div class="w-1/3 p-8">
        <LogibugLogo />
        <forgot-title/>
        <forgot-form />
      </div>
      <div class="w-2/3 bg-blue-500"></div>
    </div>
  </template>
  
  <script>
  
  import ForgotTitle from '../components/Forget/ForgotTitle.vue';
  import ForgotForm from '../components/Forget/ForgotForm.vue';
  import LogibugLogo from '../components/major/LogibugLogo.vue';
  
  export default {
    components: {
      LogibugLogo,
      ForgotTitle,
      ForgotForm,
    }
  }
  </script>
  
  <style lang="scss" scoped></style>