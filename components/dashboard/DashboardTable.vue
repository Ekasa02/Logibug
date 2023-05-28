<template>
  <div class="list-container">
    <div class="max-h-[40vh] overflow-y-auto">
      <ul class="list-group h-full py-4">
        <li class="list-group-item mb-2" v-for="item in items" :key="item.id">
          <div class="flex w-full justify-between border-b border-solid py-2 hover:cursor-pointer" @click="toCreateVersion(item.id)">
            <div class="flex items-center">
              <div class="py-2">
                <img src="./svg/List.svg" alt="List Icon" class="h-full">
              </div>
              <div class="flex flex-col ml-3 items">
                <h5 v-if="item.name" class="text-sm font-semibold text-gray-700">
                  <span class="text-gray-700 font-semibold text-sm">{{ item.name }}</span>
                </h5>
                <div class="flex gap-x-4 items-center mt-2">
                  <div v-if="item.platform === 'mobile'" class="text-gray-300">
                    <div>
                      <img src="./svg/Mobile.svg" alt="List Icon" class="h-full">
                    </div>
                  </div>
                  <div v-if="item.platform === 'web'" class="text-gray-300">
                    <div>
                      <img src="./svg/Web.svg" alt="List Icon" class="h-full">
                    </div>
                  </div>
                  <div v-if="item.type_test === 'manual'" class="rounded-lg border-gray-300 border-2 border-solid px-4">
                    <p class="text-gray-700">Manual</p>
                  </div>
                  <div v-if="item.type_test === 'automatic'" class="rounded-lg border-gray-300 border-2 border-solid px-4">
                    <p class="text-gray-700 text-sm">Automatic</p>
                  </div>
                </div>
              </div>
            </div>
            <div class="flex items-center gap-x-4 mr-4">
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
    </div>
    <div v-if="!items.length" class="flex justify-center">
      <img src="./svg/NoProject.svg" alt="No items found." class="h-[200px]">
    </div>
    <PopupEdit v-if="isEditVisible" :item="selectedItem" @closePopup="closeEdit" />
  </div>
</template>

<script>
import PopupEdit from '../projectedit/editproject/PopupEdit.vue';

export default {
  components: { PopupEdit },
  props: {
    items: {
      type: Array,
      default: () => []
    }
  },
  data() {
    return {
      isEditVisible: false,
      selectedItem: null
    };
  },
  methods: {
    editPopup(item) {
      this.selectedItem = item;
      this.isEditVisible = true;
    },
    async deleteItem(id) {
      try {
        const response = await this.$axios.delete(`/projects/${id}`);
        console.log(response);
      } catch (error) {
        console.log(error);
      }
    },
    closeEdit() {
      this.isEditVisible = false;
      // Additional logic or actions after closing the edit popup
    },
    toCreateVersion(id) {
      this.$router.push(`/createversion/${id}`);
    }
  },
};
</script>
