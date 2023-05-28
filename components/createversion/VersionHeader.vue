<template>
    <div>
        <div class="flex items-center justify-end py-[14px] pr-[100px] border-b-[1px] border-gray-300">
            <div class="ml-auto">
                <LogibugProfile @click="openProfile" />
            </div>
        </div>
        <DashboardPopup v-if="isProfileVisible" @openProfile="openProfile" />
    </div>
</template>
  
<script>
import LogibugProfile from '../major/LogibugProfile.vue';
import DashboardPopup from '../dashboard/DashboardPopup.vue';

export default {
    components: { LogibugProfile, DashboardPopup },
    data() {
        return {
            isProfileVisible: false
        }
    },
    methods:{
        openProfile(){
            this.isProfileVisible = true;
        }
    }
}
</script>

<style lang="scss" scoped></style>