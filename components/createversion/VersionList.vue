<template>
  <div>
    <ul class="list-group h-full mt-[50px]">
      <li v-for="item in items" :key="item.id" class="list-group-item mb-2" >
        <div
          class="border-b border-gray-200 flex justify-between pb-[20px] hover:cursor-pointer"
          @click="toCreateVersion(item.id)"
        >
          <div class="flex">
            <h1 class="font-semibold text-xl">{{ item.name }}</h1>
          </div>
          <div class="flex gap-x-3 items-center">
            <div @click="deleteProject">
              <button @click="deleteItem(item.id)">
                <img
                  src="./svg/Delete.svg"
                  alt="List Icon"
                  class="h-[20px] w-[20px]"
                />
              </button>
            </div>
            <DeletePopup v-if="isPopupDelete" @deleteProject="deleteProject" />
            <img
              src="./svg/Copy.svg"
              alt="List Icon"
              class="h-[20px] w-[20px]"
            />
            <button @click="editPopup(item)">
              <img
                src="./svg/Edit.svg"
                alt="List Icon"
                class="h-[20px] w-[20px]"
              />
            </button>
          </div>
        </div>
      </li>
    </ul>
    <VersionEdit
      v-if="isEditVisible"
      :item="selectedItem"
      @closePopup="closePopup"
    />
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
