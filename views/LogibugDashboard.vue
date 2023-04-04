<template>
    <div>
        <DashboardProfile />
        <DashboardTitle user-name="John" />
        <DashboardProject />
        <div class="flex justify-between">
            <DashboardSearch />
            <DashboardButton />
        </div>
        <DashboardTable :projects="projects" />
    </div>
</template>

<script>
import DashboardButton from '../components/dashboard/DashboardCreateproject.vue';
import DashboardProfile from '../components/dashboard/DashboardProfile.vue';
import DashboardSearch from '../components/dashboard/DashboardSearchproject.vue';
import DashboardTitle from '../components/dashboard/DashboardTitle.vue';
import DashboardProject from '../components/dashboard/DashboardProject.vue';
import DashboardTable from '../components/dashboard/DashboardTable.vue';

export default {
    components: { DashboardProfile, DashboardTitle, DashboardSearch, DashboardButton, DashboardProject, DashboardTable },
    data() {
        return {
            projects: [
                {
                    name: "Project 1",
                    lastEdited: "2022-01-01",
                    createdBy: "John Doe"
                },
                {
                    name: "Project 2",
                    lastEdited: "2022-02-01",
                    createdBy: "Jane Smith"
                },
                {
                    name: "Project 3",
                    lastEdited: "2022-03-01",
                    createdBy: "Bob Johnson"
                }
            ]
        }
    },
}

</script>

<style lang="scss" scoped></style>