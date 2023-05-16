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
                            <h5 v-if="item.name" class="text-sm font-semibold text-gray-700">
                                <nuxt-link
                                    :to="{ path: '/createversion', query: { name: item.name, description: item.description, platform: item.platform, type_test: item.type_test } }">
                                    <span class="text-gray-700 font-semibold text-sm">{{ item.name }}</span>
                                </nuxt-link>
                            </h5>
                            <div class="flex gap-x-4 items-center">
                                <h5 class=" text-gray-700 font-sm">
                                    <span v-if="item.description" :id="'project-version-' + item.id"
                                        class="text-gray-400 font-semibold">{{ item.description }}</span>
                                </h5>
                                <div v-if="item.platform === 'Mobile'" class="text-gray-300">
                                    <div>
                                        <img src="./svg/Mobile.svg" alt="List Icon" class="h-full">
                                    </div>
                                </div>
                                <div v-if="item.platform === 'Web'" class="text-gray-300">
                                    <div>
                                        <img src="./svg/Web.svg" alt="List Icon" class="h-full">
                                    </div>
                                </div>
                                <div v-if="item.type_test === 'Manual'"
                                    class="rounded-lg border-gray-300 border-2 border-solid px-4">
                                    <p class="text-gray-700">Manual</p>
                                </div>
                                <div v-if="item.type_test === 'Automatic'"
                                    class="rounded-lg border-gray-300 border-2 border-solid px-4">
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
    props: {
        items: {
            type: Array,
            default: () => []
        }
    },
    data() {
        return {

        };
    },
};
</script>
  