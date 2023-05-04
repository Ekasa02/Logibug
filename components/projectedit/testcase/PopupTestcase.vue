<template>
  <div class="bg-[#33333385] fixed top-0 left-0 right-0 bottom-0 flex items-center sm:justify-center font-['monserrat']">
    <div>
      <div class="bg-white rounded-lg shadow-lg">
        <header-create></header-create>
        <div class="pl-5 pr-5">
          
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HeaderCreate from './HeaderCreate.vue';


export default {
  components: {
    HeaderCreate,
    
  },
}
</script>
