<template>
    <div>
        <VersionHeader />
        <div class="px-[100px] py-[50px]">
            <div class="flex justify-between">
                <VersionName project-name="Logibug" platform="Mobile" type-test="Manual"/>
                <VersionButton />
            </div>
            <VersionList />
        </div>
    </div>
</template>

<script>
import VersionHeader from '../components/createversion/VersionHeader.vue';
import VersionName from '../components/createversion/VersionName.vue';
import VersionButton from '../components/createversion/VersionButton.vue'
import VersionList from '../components/createversion/VersionList.vue';

export default {
    components: { VersionHeader, VersionName, VersionButton, VersionList },
    layout: "SidebarLayout",
}
</script>

<style lang="scss" scoped></style>