<template>
    <div class="bg-[#33333385] fixed top-0 left-0 right-0 bottom-0 flex items-center justify-center">
        <div class="bg-white p-8 rounded-lg shadow-lg">
            <div class="">
                <img src="../assets/CloseCircle.svg" alt="image" class="cursor-pointer float-right" @click="deleteProject">
            </div>
            <div class="pl-14 ">
                <img class="" src="../assets/Delete.svg" alt="image">
            </div>
            <p class="text-center pt-7 font-montserrat text-[20px]">Are you sure you want to delete the project?</p>
            <div class="flex pt-[30px] justify-center items-center gap-x-5">
                <button
                    class="bg-[#FFFFFF] font-['Montserrat'] text-[#554AF0] font-bold py-2 px-4 rounded border border-[#554AF0] hover:text-white hover:bg-red-500"
                    @click="cancelDelete">
                    Cancel
                </button>
                <button class="font-['Montserrat'] bg-[#554AF0] text-white font-bold py-2 px-4 rounded" @click="deleteItem">
                    Delete
                </button>
            </div>
        </div>
    </div>
</template>
  
<script>
export default {
    props: {
        item: {
            // Declare the item prop and its type here
            type: Number,
            required: true,
        },
    },
    methods: {
        deleteProject() {
            this.$emit("deleteProject", this.item);
        },
        async deleteItem() {
            try {
                const response = await this.$axios.delete(`/projects/${this.item}`);
                console.log(response);
                window.location.reload();
                // Additional logic or actions after deleting the item
            } catch (error) {
                console.log(error);
            }
            this.isPopupDelete = false;
        },
        cancelDelete() {
            this.$emit("cancelDelete");
        },
    },
};
</script>
  