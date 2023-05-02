<template>
    <div>
        <ul class="list-group h-full py-4">
            <li class="list-group-item mb-2" v-for="item in items" :key="item.id">
                <div class="flex w-full justify-between border-b border-solid py-2">
                    <div class="flex items-center">
                        <div class="py-2">
                            <img src="./svg/List.svg" alt="List Icon" class="h-full">
                        </div>
                        <div class="flex flex-col ml-3 items">
                            <h5 v-if="item.projectTitle" class="text-sm font-semibold text-gray-700">
                                <span class="text-gray-700 font-semibold text-sm">{{ item.projectTitle }}</span>
                            </h5>
                            <div class="flex gap-x-4 items-center">
                                <h5 class=" text-gray-700 font-sm">
                                    <span v-if="item.projectVersion" :id="'project-version-' + item.id"
                                        class="text-gray-400 font-semibold">{{ item.projectVersion }}</span>
                                </h5>
                                <div v-if="item.projectPlatform === 'Mobile'" class="text-gray-300">
                                    <div>
                                        <img src="./svg/Mobile.svg" alt="List Icon" class="h-full">
                                    </div>
                                </div>
                                <div v-if="item.projectPlatform === 'Web'" class="text-gray-300">
                                    <div>
                                        <img src="./svg/Web.svg" alt="List Icon" class="h-full">
                                    </div>
                                </div>
                                <div v-if="item.projectTesting === 'Manual'" class="rounded-lg border-gray-300 border-2 border-solid px-4">
                                    <p class="text-gray-700">Manual</p>
                                </div>
                                <div v-if="item.projectTesting === 'Automatic'" class="rounded-lg border-gray-300 border-2 border-solid px-4">
                                    <p class="text-gray-700 text-sm">Automatic</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="flex items-center">
                        <img src="./svg/Action.svg" alt="List Icon" class="h-full">
                    </div>
                </div>
            </li>
        </ul>
        <div v-if="!items.length" class="flex justify-center">
            <img src="./svg/NoProject.svg" alt="No items found." class="h-[200px]">
        </div>
    </div>
</template>
    
<script>
export default {
    data() {
        return {
            items: [
                // { id: "Item 1", projectTitle: "Logibug v1", projectVersion: "Testing version 1", projectPlatform: "Web", projectTesting: "Manual" },
                // { id: "Item 2", projectTitle: "Logibug v1", projectVersion: "Testing version 1", projectPlatform: "Mobile", projectTesting: "Manual" },
            ]
        };
    },
    mounted() {
        // Fetch the items here to populate the list
        fetch("https://example.com/items")
            .then((response) => response.json())
            .then((data) => {
                this.items = data.items;
            });
    }
};
</script>
  