<template>
  <div>
    <VersionHeader />
    <div class="px-[100px] py-[50px]">
      <div class="flex justify-between">
        <VersionName project-name="Logibug" platform="Mobile" type-test="Manual" />
        <div class="flex gap-x-4">
          <button
            class="bg-[#FFFFFF] text-[#554AF0] font-bold py-2 px-4 rounded border border-[#554AF0] hover:text-white hover:bg-red-500"
            @click="infoInvite">
            Invite
          </button>
          <PopupInvite v-if="isPopupInvite" :id="id" @inviteMember="inviteMember" />
          <button class="bg-[#554AF0] text-white font-bold py-2 px-4 rounded" @click="showCreate">
            Create version
          </button>
        </div>
      </div>
      <VersionCreate v-if="isCreateVisible" :id="id" @hideCreate="hideCreate" />
      <VersionList :items="items" />
    </div>
  </div>
</template>

<script>
import PopupInvite from '../../components/projectedit/invitemember/PopupInvite.vue';
import VersionHeader from '../../components/createversion/VersionHeader.vue';
import VersionName from '../../components/createversion/VersionName.vue';
import VersionList from '../../components/createversion/VersionList.vue';
import VersionCreate from '../../components/createversion/VersionCreate.vue';

export default {
  components: {
    PopupInvite,
    VersionHeader,
    VersionName,
    VersionList,
    VersionCreate,
  },
  layout: 'SidebarLayout',
  data() {
    return {
      isCreateVisible: false,
      id: this.$route.params.id,
      items: [],
      isPopupInvite: false,
    }
  },
  mounted() {
    this.getVersion()
  },
  methods: {
    showCreate() {
      this.isCreateVisible = true
    },
    infoInvite() {
      this.isPopupInvite = true
    },
    hideInvite() {
      this.isPopupInvite = false
    },
    hideCreate() {
      this.isCreateVisible = false
    },
    async getVersion() {
      try {
        const response = await this.$axios.$get(
          `/versions/?project_id=${this.id}`
        )
        console.log(response)
        this.items = response.data
      } catch (e) {
        console.log(e)
      }
    },
  },
}
</script>

<style lang="scss" scoped></style>
