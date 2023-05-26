<template>
    <div>
        <TestHeader />
        <div class="px-[100px] py-[50px]">
            <div class="flex justify-between">
                <TestName test-name="LogiBug" />
                <button class="bg-[#554AF0] text-white font-bold py-2 px-4 rounded" @click="showCreate">Create test
                    case</button>
            </div>
            <TestCreate v-if="isCreateVisible" :id="id" :scenario-id="items[0].scenario_id" @hideCreate="hideCreate" />
            <TestList :items="items" />
        </div>
    </div>
</template>

<script>
import TestHeader from '../../components/testcase/TestHeader.vue';
import TestName from '../../components/testcase/TestName.vue';
import TestList from '../../components/testcase/TestList.vue';
import TestCreate from '../../components/testcase/TestCreate.vue';

export default {
    components: { TestHeader, TestName, TestList, TestCreate },
    layout: "SidebarLayout",
    data() {
        return {
            isCreateVisible: false,
            id: this.$route.params.id,
            items: []
        }
    },
    mounted() {
        this.getTestcase();
    },
    methods: {
        showCreate() {
            this.isCreateVisible = true;
        },
        hideCreate() {
            this.isCreateVisible = false;
        },
        async getTestcase() {
            try {
                const response = await this.$axios.$get(`/test_cases/?version_id=${this.id}`)
                console.log(response)
                this.items = response.data
                console.log(this.items[0].scenario_id)
            } catch (e) {
                console.log(e)
            }
        }
    },
}
</script>

<style lang="scss" scoped></style>