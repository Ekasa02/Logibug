<template>
  <div class="bg-[#EDF1FF]">
    <div class="pl-[403px] pr-[405px] pt-[50px]">
      <text-page></text-page>
    </div>
    <div class="flex-1 flex align-items-center justify-end">
      <div class="mr-[70px] mt-[70px]">
        <text-box></text-box>
      </div>
      <div class="ml-[20px] ">
        <img src="../assets/images/icon/Group 1.svg" alt="logo" class="object-cover" >
      </div>
    </div>
    <div class="flex-1 flex align-items-center justify-end">
      <div class="pl-[3px] pr-[100px] pt-2 ">
        <img src="../assets/images/icon/Group 2.svg" alt="logo" class="object-cover" >
      </div>
      <div class="mr-[50px] mt-[70px] pt-[60px]">
        <text-box></text-box>
      </div>
    </div>
    <div class="flex-1 flex align-items-center justify-end">
      <div class="mr-[70px] mt-[70px] pt-[60px]">
        <text-box></text-box>
      </div>
      <div class="ml-[20px] mr-[100px] ">
        <img src="../assets/images/icon/Group 3.svg" alt="logo" class="object-cover" >
      </div>
    </div>
  </div>



  
</template>

<script>
  import TextBox from '../components/landingpage/TextBox.vue';
  import TextPage from '../components/landingpage/TextPage.vue';
  
  export default {
    components: {
      TextBox,
      TextPage,
    },
  };
</script>

<style>

</style>
