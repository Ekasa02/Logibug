<template>
  <div>
    <div class="max-h-[40vh] overflow-y-auto">
      <ul class="list-group h-full py-4">
        <li v-for="item in items" :key="item.id" class="list-group-item mb-2">
          <div class="flex w-full justify-between border-b border-solid py-2 hover:cursor-pointer"
            @click="toCreateVersion(item.id)">
            <div class="flex items-center">
              <div class="py-2">
                <img src="./svg/List.svg" alt="List Icon" class="h-full">
              </div>
              <div class="flex flex-col ml-3 items">
                <h5 v-if="item.name" class="text-sm font-semibold text-gray-700">
                  <span class="text-gray-700 font-semibold text-sm">{{ item.name
                  }}</span>
                </h5>
                <div class="flex gap-x-4 items-center">
                  <h5 class="text-gray-700 font-sm">
                    <span v-if="item.description" :id="'project-version-' + item.id" class="text-gray-400 font-semibold">
                      {{ item.description }}
                    </span>
                  </h5>
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
                  <div v-if="item.type_test === 'automatic'"
                    class="rounded-lg border-gray-300 border-2 border-solid px-4">
                    <p class="text-gray-700 text-sm">Automatic</p>
                  </div>
                </div>
              </div>
            </div>
            <div class="flex items-center gap-x-4 mr-5">
              <button @click="deleteProject(item.id); $event.stopPropagation()">
                <img src="./svg/Delete.svg" alt="List Icon" class="h-[20px] w-[20px]">
              </button>
              <button @click="editPopup(item); $event.stopPropagation()">
                <img src="./svg/Edit.svg" alt="List Icon" class="h-[20px] w-[20px]">
              </button>
            </div>
            <DashboardDelete v-if="isPopupDelete" :item="deleteItemId" @deleteProject="hideDelete" />
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
import DashboardDelete from './DashboardDelete.vue';

export default {
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
      isPopupDelete: false,
      deleteItemId: null,
    };
  },
  methods: {
    editPopup(item) {
      this.selectedItem = item;
      this.isEditVisible = true;
    },
    deleteProject(id) {
      this.deleteItemId = id;
      this.isPopupDelete = true;
    },
    hideDelete() {
      this.isPopupDelete = false;
    },
    // async deleteItem() {
    //   try {
    //     const response = await this.$axios.delete(`/projects/${this.deleteItemId}`);
    //     console.log(response);
    //     // Additional logic or actions after deleting the item
    //   } catch (error) {
    //     console.log(error);
    //   }
    //   this.isPopupDelete = false;
    // },
    closeEdit() {
      this.isEditVisible = false;
      // Additional logic or actions after closing the edit popup
    },
    toCreateVersion(id) {
      this.$router.push(`/createversion/${id}`);
    }
  },
  components: { PopupEdit, DashboardDelete }
};
</script>