<template>
    <div class="flex">
        <div class="bg-gray-800 w-1/5 h-screen flex flex-col">
            <!-- Sidebar content -->
            <div class="flex-1 flex flex-col justify-start items-center text-white pt-10">
                <LogibugLogo class="text-blue-500" />
                <ul class="mt-6 text-lg font-medium">
                    <li :class="{ 'text-blue-500': $route.path === '/dashboard' }" class="mb-4">
                        <NuxtLink to="/dashboard">Home</NuxtLink>
                    </li>
                    <li :class="{ 'text-blue-500': $route.path === '/issues' }" class="mb-4">
                        <NuxtLink to="/issues">Issues</NuxtLink>
                    </li>
                    <li :class="{ 'text-blue-500': $route.path === '/report' }">
                        <NuxtLink to="/report">Report</NuxtLink>
                    </li>
                </ul>
            </div>
        </div>
        <div class="w-4/5 h-screen bg-gray-100">
            <component :is="currentRouteComponent" />
        </div>
    </div>
</template>
  
<script>
import LogibugLogo from '../components/major/LogibugLogo.vue';
import Dashboard from '../views/LogibugDashboard.vue';
// import IssuesPage from '../views/IssuesPage.vue'
// import ReportPage from '../views/ReportPage.vue'

export default {
    name: "SidebarLayout",
    components: { LogibugLogo },
    computed: {
        currentRouteComponent() {
            switch (this.$route.path) {
                case '/dashboard':
                    return Dashboard
                // case '/issues':
                //     return IssuesPage
                // case '/report':
                //     return ReportPage
                default:
                    return Dashboard
            }
        }
    }
}
</script>
  
<style lang="scss" scoped></style>
  