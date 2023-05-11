<template>
    <div>
        <div class="flex items-center justify-end py-[14px] pr-[100px] border-b-[1px] border-gray-300">
            <div @click="handleProfileClick" class="ml-auto">
                <LogibugProfile :isPopupVisible="PopupVisible" @click="Popup = true" />
            </div>
        </div>
        <DashboardPopup v-if="isPopupVisible" @close="isPopupVisible = false"/>
    </div>
</template>
  
<script>
import LogibugProfile from '../major/LogibugProfile.vue';
import DashboardPopup from './DashboardPopup.vue';

export default {
    components: { LogibugProfile, DashboardPopup },
    data() {
        return {
            isPopupVisible: this.popupVisible
        }
    },
    props:{
        PopupVisible:{
            type: Boolean,
            required: true
        }
    },
    methods:{
        handleProfileClick(){
            this.$emit('click', true);
        }
    },
    created() {
  this.Popup = this.isPopupVisible;
},
}
</script>

<style lang="scss" scoped></style>