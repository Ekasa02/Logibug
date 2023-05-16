<template>
    <div>
        <ul class="list-group h-full mt-[50px]">
            <li class="list-group-item">
                <div class="border-b border-gray-200 flex justify-between pb-[20px]">
                    <div class="flex">
                        <h1 class="font-semibold text-xl">Test</h1>
                    </div>
                    <div class="flex gap-x-3 items-center">
                        <img src="./svg/Delete.svg" alt="List Icon" class="h-[20px] w-[20px]">
                        <img src="./svg/Copy.svg" alt="List Icon" class="h-[20px] w-[20px]">
                        <img src="./svg/Edit.svg" alt="List Icon" class="h-[20px] w-[20px]">
                    </div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    props: {
        versions: {
            type: Array,
            default: () => []
        }
    },
    data() {
        return {

        };
    },
}
</script>

<style lang="scss" scoped></style>