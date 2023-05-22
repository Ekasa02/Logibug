<template>
    <div>
        <SettingProfile @showProfile="showProfile"/>
        <div class=" bg-[#FBFBFC] md:px-4 md:py-3 ">
            <DashboardPopup v-if="isProfileVisible" />
            <div class="md:rounded-[20px] bg-white border border-solid border-[#EFEFF0] px-[40px] w-full">
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