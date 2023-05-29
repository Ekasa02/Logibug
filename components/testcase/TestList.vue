<template>
  <div>
    <ul class="list-group h-full mt-[50px]">
      <li class="list-group-item" v-for="item in items" :key="item.id">
        <div class="border-b border-gray-200 pb-[20px] flex gap-x-5 hover:cursor-pointer" @click="toDetailTest(item.version_id)">
          <div class="w-[10px] h-[70px] rounded-xl bg-[#B3B3B3]"></div>
          <div>
            <h1 class="font-semibold text-xl">{{ item.testcase }}</h1>
            <div class="flex mt-2 gap-x-2">
              <div class="bg-[#8787F8] px-[20px] py-[2px] rounded-xl text-white">Login</div>
              <div class="bg-[#FCD051] px-[20px] py-[2px] rounded-xl text-white">Positif</div>
            </div>
          </div>
          <div class="flex gap-x-3 items-center ml-auto">
            <button @click="deleteItem(item.id); $event.stopPropagation()">
              <img src="./svg/Delete.svg" alt="List Icon" class="h-[20px] w-[20px]">
            </button>
            <button @click="editPopup(item); $event.stopPropagation()">
              <img src="./svg/Edit.svg" alt="List Icon" class="h-[20px] w-[20px]">
            </button>
          </div>
        </div>
      </li>
    </ul>
    <TestEdit v-if="isEditVisible" :id="id" :item="selectedItem" @closePopup="closePopup" />
  </div>
</template>
  
<script>
import TestEdit from './TestEdit.vue';
export default {
  components: {
    TestEdit
  },
  props: {
    items: {
      type: Array,
      default: () => []
    }
  },
  data() {
    return {
      isEditVisible: false,
      selectedItem: null,
      id: '',
    };
  },
  methods: {
    editPopup(item) {
      this.selectedItem = item;
      this.id = item.id;
      this.isEditVisible = true;
    },
    closePopup() {
      this.isEditVisible = false;
    },
    toDetailTest(id) {
      this.$router.push(`/detailtest/${id}`)
    }
  }
}
</script>
  
<style lang="scss" scoped></style>
  