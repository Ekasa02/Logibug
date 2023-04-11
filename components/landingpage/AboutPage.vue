<template>
  <div class="bg-[#EDF1FF] py-[70px]">
    <TextPage />
    <div class="flex-1 flex align-items-center justify-center items-center gap-x-[40px] mt-[40px]">
      <div class="text-center font-montserrat">
        <h1 class="text-3xl font-bold pb-[50px]">Access Logibug anytime and <br /> anywhere</h1>
        <p class="text-[20px]">Available in both web and mobile app versions, you can <br />
          easily access LogiBug anytime, anywhere. Take full <br /> control of your testing project, monitor progress
          easily, <br /> and efficiently manage your team</p>
      </div>
      <img src="../assets/ContentImage1.svg" alt="logo" class="object-cover">
    </div>

    <div class="flex-1 flex align-items-center justify-center items-center gap-x-[40px]">
      <img src="../assets/ContentImage2.svg" alt="logo" class="object-cover">
      <div class="text-center font-montserrat">
        <h1 class="text-3xl font-bold pb-[50px]">LogiBug has two testing methods <br /> that you can use</h1>
        <p class="text-[20px]">LogiBug is a software testing application that provides two <br />
          main services: manual testing and API testing. With <br /> comprehensive and user-friendly features, Logibug
          will help <br /> you save time and maximize productivity in testing.</p>
      </div>
    </div>

    <div class="flex-1 flex align-items-center justify-center items-center gap-x-[40px]">
      <div class="text-center font-montserrat">
        <h1 class="text-3xl font-bold pb-[50px]">Collaborate With Teams</h1>
        <p class="text-[20px]">Together with the testing team, you can collaborate to <br />
          perform software testing. You can easily collaborate with <br /> programmers in identifying and resolving
          issues, thus <br /> speeding up the testing project completion time.</p>
      </div>
      <img src="../assets/ContentImage3.svg" alt="logo" class="object-cover">
    </div>
  </div>
</template>

<script>
import TextPage from './TextPage.vue';

export default {
  components: {
    TextPage,
  },
};
</script>

<style></style>
