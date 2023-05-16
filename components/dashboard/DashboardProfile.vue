<template>
   <div 
    class="bg-[#33333385] fixed top-16  right-0 transform -translate-x-28"
  >
    <div >
      <div class="bg-white rounded-lg shadow-lg">
        <div class=" pt-2 ">
            <h1 class="font-bold font-Montserrat text-2xl pl-9">Account</h1>
            <hr class=" border-gray-300 my-4 w-full">
        </div>
        <div class="pl-5">
            <div class="bg-white rounded-lg  overflow-hidden">
                <div class="flex flex-row items-center p-2">
                  <div class="w-1/4 ml-3">
                    <img src="../assets/Profil.svg" class="w-full h-auto rounded-full" alt="Profile picture">
                  </div>
                  <div class="w-3/4 pl-6 pr-20 ">
                    <h2 class="text-xl font-bold">Eka Safitri</h2>
                    <p>@Eka_s.a</p>
                  </div>
                </div>
              </div>
        </div>
        <div>
            <div
              class="ml-10 rounded-[28px] px-6 py-2 w-[120px] flex items-center justify-center mt-3 text-white font-semibold text-sm bg-[#DD00D2]"
            >
              <h1>Beginner</h1>
            </div>
            <div class="pl-10">
              <p class="pt-2 pr-5">
                50 Issue telah di uji. selesaikan 150 issue lagi untuk <br />mencapai
                tingkat menengah
              </p>
            </div>
            <hr class="border-gray-300 my-4 w-full" />
            <div>
              <div class="flex pt-2 text-[16px] pl-10">
                <img src="../assets/Setting.svg" />
                <p class="pl-3">Account Setting</p>
              </div>
              <hr class="border-gray-300 my-4 w-full" />
              <div class="flex pt-2 text-[16px] pl-10">
                <img src="../assets/Achievment.svg" />
                <p class="pl-3">Achievement</p>
              </div>
              <hr class="border-gray-300 my-4 w-full" />
              <div class="flex pt-2 text-[16px] pl-10">
                <img src="../assets/InfoCircle.svg" />
                <p class="pl-3">About</p>
              </div>
              <hr class="border-gray-300 my-4 w-full" />
              <div class="flex pt-2 text-[16px] pb-5 pl-10">
                <img src="../assets/Logout.svg" />
                <p class="pl-3">Log Out</p>
              </div>
            </div>
          </div>
      </div>
    </div>
  </div>

</template>
  
<script>
// import LogibugProfile from '../major/LogibugProfile.vue';
// import DashboardPopup from './DashboardPopup.vue';

export default {
    // components: { LogibugProfile, DashboardPopup },
    data(){
        return{
            isPopupProfile: false
        }
    },
    methods:{
        openProfile(){
            this.$emit('openProfile', true)
        },
        closeProfile(){
            this.isPopupProfile = false
        }
    },
}
</script>

<style lang="scss" scoped></style>