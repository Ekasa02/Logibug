<template>
    <div>
        <ul class="list-group h-full mt-[50px]">
            <li class="list-group-item mb-2" v-for="item in items" :key="item.id">
                <div class="border-b border-gray-200 flex justify-between pb-[20px]">
                    <div class="flex">
                        <h1 class="font-semibold text-xl">Test</h1>
                    </div>
                    <div class="flex gap-x-3 items-center">
                        <img src="./svg/Delete.svg" alt="List Icon" class="h-[20px] w-[20px]">
                        <img src="./svg/Copy.svg" alt="List Icon" class="h-[20px] w-[20px]">
                        <button @click="editPopup(item)">
                            <img src="./svg/Edit.svg" alt="List Icon" class="h-[20px] w-[20px]">
                        </button>
                    </div>
                </div>
            </li>
        </ul>
        <VersionEdit v-if="isEditVisible" :item="selectedItem" @closePopup="closeEdit" />
    </div>
</template>

<script>
import VersionEdit from './VersionEdit.vue';

export default {
    components: { VersionEdit },
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
    },
}
</script>

<style lang="scss" scoped></style>