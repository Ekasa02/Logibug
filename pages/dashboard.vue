<template>
    <div>
        <div class="flex items-center justify-end py-[14px] pr-[100px] border-b-[1px] border-gray-300">
            <div class="ml-auto">
                <DashboardProfile @showProfile="showProfile" />
            </div>
        </div>
        <div class="px-[20%] md:px-[100px]">
            <DashboardPopup v-if="isProfileVisible" />
            <DashboardTitle user-name="John" />
            <DashboardLevel level="Beginner" />
            <DashboardProject />
            <div class="md:flex justify-between" style="margin-top: 15px;">
                <DashboardSearch />
                <DashboardButton @showPopup="showPopup" />
            </div>
            <PopupCreate v-if="isPopupVisible" @closePopup="closePopup" @submit="createProject" />
        </div>
        <div style="padding: 20px 100px;">
            <DashboardTable :items="items" />
        </div>
        <nuxtLink to="/tes/10">tes</nuxtLink>
    </div>
</template>
<script>
import DashboardButton from '../components/dashboard/DashboardCreateproject.vue';
import DashboardPopup from '../components/dashboard/DashboardPopup.vue';
import DashboardSearch from '../components/dashboard/DashboardSearchproject.vue';
import DashboardTitle from '../components/dashboard/DashboardTitle.vue';
import DashboardProject from '../components/dashboard/DashboardProject.vue';
import DashboardTable from '../components/dashboard/DashboardTable.vue';
import DashboardLevel from '../components/dashboard/DashboardLevel.vue';
import PopupCreate from '../components/projectedit/createproject/PopupCreate.vue';
import DashboardProfile from '../components/dashboard/DashboardProfile.vue';

export default {
    components: {
        DashboardProfile,
        DashboardTitle,
        DashboardPopup,
        DashboardSearch,
        DashboardButton,
        DashboardProject,
        DashboardTable,
        DashboardLevel,
        PopupCreate,
    },
    layout: 'SidebarLayout',
    data() {
        return {
            isPopupVisible: false,
            isProfileVisible: false,
            items: [
                // { id: "Item 1", projectTitle: "Logibug v1", projectVersion: "Testing version 1", projectPlatform: "Web", projectTesting: "Manual" },
                // { id: "Item 2", projectTitle: "Logibug v1", projectVersion: "Testing version 1", projectPlatform: "Mobile", projectTesting: "Manual" },
            ]
        }
    },
    methods: {
        showPopup() {
            this.isPopupVisible = true;
        },
        closePopup() {
            this.isPopupVisible = false;
        },
        showProfile() {
            this.isProfileVisible = !this.isProfileVisible;
        },
        createProject(project) {
            console.log('run', project)
            // console.log(project))

            project.id = this.items.length + 1;
            this.items.push(project);
        },
        tes() {
            console.log('testing')
        },
        async getProject() {
            try {
                const response = await this.$axios.$get('/projects')
                console.log(response)
                this.items = response.data
            } catch (e) {
                console.log(e)
            }
        }
    },
    mounted() {
        this.getProject();
    },
}
</script>