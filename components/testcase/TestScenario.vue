<template>
    <div class="bg-[#33333385] fixed top-0 left-0 right-0 bottom-0 flex items-center sm:justify-center">
        <div class="bg-white p-8 rounded-lg shadow-lg">
            <div class="flex">
                <h1 class="font-Montserrat font-bold text-2xl pr-[300px]">Scenario</h1>
                <img src="../createversion/svg/CloseCircle.svg" class="cursor-pointer" alt="Close Icon" @click="closeModal">
            </div>
            <hr class="border-gray-300 my-4 w-full">
            <form @submit.prevent="postProject">
                <div class="relative pt-[15px]">
                    <label class="block font-Montserrat font-bold text-[14px] mb-2" for="scenario">
                        Add Scenario
                    </label>
                    <div class="flex items-center">
                        <input
                            id="scenario"
                            class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                            type="text" placeholder="Scenario" />
                        <button
                            class="hover:opacity-80 text-white font-bold py-2 px-2.5 bg-blue-500 rounded ml-3 border border-gray-300">
                            Create
                        </button>
                    </div>
                </div>
            </form>
            <div class="mt-[25px]">
                <p class="block font-Montserrat font-bold text-[14px] mb-2">Scenario list</p>
                <ul class="list-group h-full mt-[50px]">
                    <li v-for="item in items" :key="item.id" class="list-group-item mb-2">
                        <div class="border-b border-gray-200 flex justify-between pb-[20px]">
                            <div class="flex">
                                <h1 class="font-semibold text-xl">{{ item.name }}</h1>
                            </div>
                            <div class="flex gap-x-3 items-center">
                                <button @click="deleteItem(item.id)">
                                    <img src="./svg/Delete.svg" alt="List Icon" class="h-[20px] w-[20px]">
                                </button>
                                <button @click="editPopup(item)">
                                    <img src="./svg/Edit.svg" alt="List Icon" class="h-[20px] w-[20px]">
                                </button>
                            </div>
                        </div>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>
  
<script>
export default {
    props: {
        id: {
            type: String,
            required: true
        },
    },
    data() {
        return {
            items: [],
            projectId: '',
        };
    },
    mounted() {
        this.getScenario();
    },
    methods: {
        closeModal() {
            this.$emit("hideScenario");
        },
        async getScenario() {
            try {
                const response = await this.$axios.$get(`/scenarios/?project_id=122`);
                console.log(response);
                this.items = response.data;
            } catch (e) {
                console.log(e);
            }
        }
    }
};
</script>
  