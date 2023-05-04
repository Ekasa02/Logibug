<template>
    <div class="bg-[#33333385] fixed top-0 left-0 right-0 bottom-0 flex items-center sm:justify-center font-['monserrat']">
      <div>
        <div class="bg-white rounded-lg shadow-lg ">
          <header-member></header-member>
          <div class="pl-5 pr-5">
            <div>
              <div class="flex">
                <profile-name></profile-name>
                <edit-member></edit-member>
              </div>
              <hr class=" border-gray-300 my-4 w-full">
              <div class="flex">
                <profile-name></profile-name>
                <edit-member></edit-member>
              </div>
              <hr class=" border-gray-300 my-4 w-full">
              <div class="flex">
                <profile-name></profile-name>
                <edit-member></edit-member>
              </div>
              <hr class=" border-gray-300 my-4 w-full">
              <div class="flex">
                <profile-name></profile-name>
                <edit-member></edit-member>
              </div>
            </div>
            
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import HeaderMember from './HeaderMember.vue';
 import ProfileName from './ProfileName.vue';
 import EditMember from './EditMember.vue';
  
  export default {
    components: {
      HeaderMember,
      ProfileName,
      EditMember,
    },
  }
  </script>
  