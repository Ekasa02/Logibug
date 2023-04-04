<template>
    <div>
        <div class="bg-gray-200 flex items-center justify-end p-4">
            <div class="ml-auto">
                <LogibugProfile @click="showPopup = true" />
            </div>
        </div>
        <DashboardPopup v-if="showPopup" @close="showPopup = false"/>
    </div>
</template>
  
<script>
import LogibugProfile from '../major/LogibugProfile.vue';
import DashboardPopup from './DashboardPopup.vue';

export default {
    components: { LogibugProfile, DashboardPopup },
    data() {
        return {
            showPopup: false
        }
    }
}
</script>

<style lang="scss" scoped></style>