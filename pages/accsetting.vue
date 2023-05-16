<template>
    <div>
        <SettingProfile @showProfile="showProfile"/>
        <div class="px-[100px] bg-[#FBFBFC] py-[30px] ">
            <DashboardPopup v-if="isProfileVisible" />
            <div class="rounded-[20px] bg-white border border-solid border-[#EFEFF0] px-[40px]">
                <ProfilePict/>
                <EmailMember/>
                <NameProfile/>
                <ButtonSave/>
            </div>
        </div>
        
    </div>
</template>

<script>
import SettingProfile from '../components/accountsetting/SettingProfile.vue';
import DashboardPopup from '../components/dashboard/DashboardPopup.vue';
import ProfilePict from '../components/accountsetting/ProfilPict.vue';
import EmailMember from '../components/accountsetting/EmailMember.vue';
import NameProfile from '../components/accountsetting/NameProfile.vue';
import ButtonSave from '../components/accountsetting/ButtonSave.vue';

    export default {
        data(){
            return{
                isProfileVisible:false,
            }
        },
        components:{
            SettingProfile,
            DashboardPopup,
            ProfilePict,
            EmailMember,
            NameProfile,
            ButtonSave,
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