<template>
    <div>
        <SettingProfile @showProfile="showProfile"/>
        <div class="px-[100px] bg-[#FBFBFC] py-[30px] ">
            <DashboardPopup v-if="isProfileVisible" />
            <div class="rounded-[20px] bg-[#C2CFFB] border border-solid border-[#EFEFF0] px-[40px] items-center justify-center">
                <ProfilTestcase/>
                <LevelDesc/>
                <RateClass/>
            </div>
        </div>
    </div>
</template>

<script>
import SettingProfile from '../components/accountsetting/SettingProfile.vue';
import ProfilTestcase from '../components/achieve/ProfilTestcase.vue';
import LevelDesc from '../components/achieve/LevelDesc.vue';
import RateClass from '../components/achieve/RateClass.vue';

    export default {
        data(){
            return{
                isProfileVisible:false,
            }
        },
        components:{
            SettingProfile,
            ProfilTestcase,
            LevelDesc,
            RateClass,
          
        },
        methods:{
            showProfile() {
                this.isProfileVisible = !this.isProfileVisible;
            },
        },
        layout:'SidebarLayout',
    }
</script>

<style lang="scss" scoped>

</style>