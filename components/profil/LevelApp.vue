<template>
  <div>
    <div
      class="mx-5 rounded-[28px] px-6 py-2 w-[120px] flex items-center justify-center mt-3 text-white font-semibold text-sm bg-[#DD00D2]"
    >
      <h1>Beginner</h1>
    </div>
    <div class="px-5">
      <p class="pt-2 pr-5">
        50 Issue telah di uji. selesaikan 150 issue lagi untuk <br />mencapai
        tingkat menengah
      </p>
    </div>
    <hr class="border-gray-300 my-4 w-full" />
    <div class="">
      <div class="flex text-[16px] px-5">
        <img src="../assets/Setting.svg" />
        <nuxt-link to="/accsetting" class="pl-3">Account Setting</nuxt-link>
      </div>
      <hr class="border-gray-300 my-4 w-full" />
      <div class="flex text-[16px] px-5">
        <img src="../assets/Achievment.svg" />
        <p class="pl-3">Achievement</p>
      </div>
      <hr class="border-gray-300 my-4 w-full" />
      <div class="flex text-[16px] px-5">
        <img src="../assets/InfoCircle.svg" />
        <p class="pl-3">About</p>
      </div>
      <hr class="border-gray-300 my-4 w-full" />
      <div class="flex text-[16px] pb-5 px-5">
        <img src="../assets/Logout.svg" />
        <p class="pl-3">Log Out</p>
      </div>
    </div>
  </div>
</template>
