<template>
    <div>
        <ul class="list-group h-full mt-8 max-h-[70vh] overflow-y-auto">
            <li class="list-group-item mb-2" v-for="item in items" :key="item.id">
                <div class="border-b border-gray-200 flex justify-between pb-5 hover:cursor-pointer"
                    @click="toCreateVersion(item.id)">
                    <div class="flex">
                        <h1 class="font-semibold text-xl">{{ item.name }}</h1>
                    </div>
                    <div class="flex gap-3 items-center">
                        <button @click="deleteItem(item.id); $event.stopPropagation()">
                            <img src="./svg/Delete.svg" alt="List Icon" class="h-5 w-5">
                        </button>
                        <img src="./svg/Copy.svg" alt="List Icon" class="h-5 w-5">
                        <button @click="editPopup(item); $event.stopPropagation()">
                            <img src="./svg/Edit.svg" alt="List Icon" class="h-5 w-5">
                        </button>
                    </div>
                </div>
            </li>
        </ul>
        <VersionEdit v-if="isEditVisible" :item="selectedItem" @closePopup="closePopup" />
    </div>
</template>
  
<script>
import DeletePopup from '../version/deleteversion/DeletePopup.vue';
import VersionEdit from './VersionEdit.vue';

export default {
  components: { DeletePopup, VersionEdit },
  props: {
    items: {
      type: Array,
      default: () => [],
    },
  },
  data() {
    return {
      isEditVisible: false,
      selectedItem: null,
      isPopupDelete: false,
    }
  },
  methods: {
    editPopup(item) {
      this.selectedItem = item
      this.isEditVisible = true
    },
    methods: {
        editPopup(item) {
            this.selectedItem = item;
            this.isEditVisible = true;
        },
        closePopup() {
            this.isEditVisible = false;
        },
        async deleteItem(id) {
            try {
                const response = await this.$axios.delete(`/versions/${id}`);
                console.log(response);
            } catch (error) {
                console.log(error);
            }
        },
        toCreateVersion(id) {
            this.$router.push(`/testcase/${id}`);
        }
    deleteProject() {
      this.isPopupDelete = true
    },
    closePopup() {
      this.isEditVisible = false
    },
    async deleteItem(id) {
      try {
        const response = await this.$axios.delete(`/versions/${id}`)
        console.log(response)
      } catch (error) {
        console.log(error)
      }
    },
    toCreateVersion(id) {
      this.$router.push(`/testcase/${id}`)
    },
  },
}
</script>
<style lang="scss" scoped></style>
