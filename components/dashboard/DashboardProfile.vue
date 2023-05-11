<template>
    <div>
        <div class="flex items-center justify-end py-[14px] pr-[100px] border-b-[1px] border-gray-300">
            <div @click="handleProfileClick" class="ml-auto">
                <LogibugProfile :Popup="isPopupVisible" @click="isPopupVisible = true" />
            </div>
        </div>
        <DashboardPopup v-if="Popup" @close="Popup = false"/>
    </div>
</template>
  
<script>
import LogibugProfile from '../major/LogibugProfile.vue';
import DashboardPopup from './DashboardPopup.vue';

export default {
    components: { LogibugProfile, DashboardPopup },
    data() {
        return {
            isPopupVisible: this.Popup
        }
    },
    props:{
        showPopup:{
            type: Boolean,
            required: true
        }
    },
    methods:{
        handleProfileClick(){
            this.$emit('click');
        }
    }
}
</script>

<style lang="scss" scoped></style>