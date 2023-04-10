<template>
    <div class="h-screen flex">
      <div class="w-2/5 px-20 py-20">
        <LogibugLogo />
        <changepass-title/>
        <changepass-form/>
      </div>
      <div class="w-3/5 bg-blue-500"></div>
    </div>
  </template>
  
  <script>
  
  // import ChangepassTitle from '../components/changepass/ChangepassTitle.vue';
  // import ChangepassForm from '../components/changepass/ChangepassForm.vue';
   import LogibugLogo from '../components/major/LogibugLogo.vue';
  
  export default {
     components: {
       LogibugLogo,
    //   ChangepassTitle,
    //   ChangepassForm,
    }
  }
  </script>
  
  
  <style >
  
  
</style>