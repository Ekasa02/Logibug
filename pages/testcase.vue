<template>
    <div>
        <TestHeader />
        <div class="px-[100px] py-[50px]">
            <TestName test-name="LogiBug"/>
            <TestList />
        </div>
    </div>
</template>

<script>
import TestHeader from '../components/testcase/TestHeader.vue';
import TestName from '../components/testcase/TestName.vue';
import TestList from '../components/testcase/TestList.vue';

export default {
    components: { TestHeader, TestName, TestList },
    layout: "SidebarLayout",
}
</script>

<style lang="scss" scoped></style>