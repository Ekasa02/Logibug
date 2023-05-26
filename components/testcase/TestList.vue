<template>
    <div>
      <ul class="list-group h-full mt-[50px]">
        <li class="list-group-item" v-for="item in items" :key="item.id">
          <div class="border-b border-gray-200 pb-[20px] flex gap-x-5">
            <div class="w-[10px] h-[70px] rounded-xl bg-[#B3B3B3]"></div>
            <div>
              <h1 class="font-semibold text-xl">{{ item.testcase }}</h1>
              <div class="flex mt-2 gap-x-2">
                <div class="bg-[#8787F8] px-[20px] py-[2px] rounded-xl text-white">Login</div>
                <div class="bg-[#FCD051] px-[20px] py-[2px] rounded-xl text-white">Positif</div>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      items: {
        type: Array,
        default: () => []
      }
    }
  }
  </script>
  
  <style lang="scss" scoped></style>
  