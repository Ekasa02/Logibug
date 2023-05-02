<template>
    <div>
        <DashboardProfile />
        <div style="padding: 0 100px;">
            <DashboardTitle user-name="John" />
            <DashboardLevel level="Beginner" />
            <DashboardProject />
            <div class="flex justify-between" style="margin-top: 15px;">
                <DashboardSearch />
                <DashboardButton />
            </div>
        </div>
        <div style="padding: 20px 100px;">
            <DashboardTable />
        </div>
    </div>
</template>

<script>
import DashboardButton from '../components/dashboard/DashboardCreateproject.vue';
import DashboardProfile from '../components/dashboard/DashboardProfile.vue';
import DashboardSearch from '../components/dashboard/DashboardSearchproject.vue';
import DashboardTitle from '../components/dashboard/DashboardTitle.vue';
import DashboardProject from '../components/dashboard/DashboardProject.vue';
import DashboardTable from '../components/dashboard/DashboardTable.vue';
import DashboardLevel from '../components/dashboard/DashboardLevel.vue';

export default {
    components: { DashboardProfile, DashboardTitle, DashboardSearch, DashboardButton, DashboardProject, DashboardTable, DashboardLevel },
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