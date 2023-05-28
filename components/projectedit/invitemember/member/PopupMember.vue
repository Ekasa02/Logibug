<template>
    <div class="bg-[#33333385] fixed top-0 left-0 right-0 bottom-0 flex items-center sm:justify-center font-['monserrat']">
      <div>
        <div @click="infoMember" class="bg-white rounded-lg shadow-lg pb-3">
          <header-member></header-member>
          <div class="px-5 pt-2 border-b border-gray-300 border-[85%]">
            <div class="flex items-center justify-between">
              <div class="flex">
                <img src="../../../assets/Profil.svg" class="w-[50px] h-[50px]  rounded-full" alt="Profile picture">
               <div class="pl-2">
                 <h1>Eka safitri</h1>
                   <p>Frontend</p> 
               </div>
              </div>
              <div class="flex float-right justify-end mb-2">
                  <div class="">
                      <img src="../../../assets/Edit.svg" class="w-[38px] h-[38px] pt-3 rounded-full" alt="Sunting">
                  </div>
                  <div class="pl-1">
                      <img src="../../../assets/DeleteOutlined.svg" class="w-[38px] h-[38px] pt-3 rounded-full" alt="Delete">
                  </div>
              </div>
          </div>
        </div>
      </div>
    </div>
    </div>
  </template>
  
  <script>
   import HeaderMember from './HeaderMember.vue';
//  import ProfileName from './ProfileName.vue';
//  import EditMember from './EditMember.vue';
  export default {
    // Component options
    components: {
      HeaderMember,
      // ProfileName,
      // EditMember,
    },
    data(){
      return{
        items:[]
      }
    },

    mounted (){
      this.getMember();
    },
    methods:{
      infoMember(){
        this.$emit("infoMember")
      },
      async getMember() {
            try {
                const response = await this.$axios.$get('/projects')
                console.log(response)
                this.items = response.data
            } catch (e) {
                console.log(e)
            }
        }
    }
  }
  </script>
  
  