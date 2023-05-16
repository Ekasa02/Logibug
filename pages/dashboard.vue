<template>
  <div>
    <div >
      <div
        class="flex items-center justify-end py-[14px] pr-[100px] border-b-[1px] border-gray-300"
      >
     
        <div class="ml-auto">
          <div >
            <button class="rounded-full overflow-hidden"  @click="openProfile">
              <img
                class="w-12 h-12 object-cover hover:bg-blue-700"
                src="../components/major/svgs/User.svg"
                alt="Profile Picture"
              />
            </button>
          </div>
        </div>
      </div>
      <div style="padding: 0 100px">
        <dashboard-profile v-if="isPopupProfile" >
            
        </dashboard-profile>
        <DashboardTitle user-name="John" />
        <DashboardLevel level="Beginner" />
        <DashboardProject />
        <div class="flex justify-between" style="margin-top: 15px">
          <DashboardSearch />
          <DashboardButton @showPopup="showPopup" />
        </div>
        <PopupCreate
          v-if="isPopupVisible "
          @closePopup="closePopup"
          @submit="createProject"
          @create="closePopup"
        />
      </div>
      <div style="padding: 20px 100px">
        <DashboardTable :items="items" />
      </div>
    </div>
  </div>
</template>

<script>
import DashboardButton from '../components/dashboard/DashboardCreateproject.vue'
import DashboardProfile from '../components/dashboard/DashboardProfile.vue'
import DashboardSearch from '../components/dashboard/DashboardSearchproject.vue'
import DashboardTitle from '../components/dashboard/DashboardTitle.vue'
import DashboardProject from '../components/dashboard/DashboardProject.vue'
import DashboardTable from '../components/dashboard/DashboardTable.vue'
import DashboardLevel from '../components/dashboard/DashboardLevel.vue'
import PopupCreate from '../components/projectedit/createproject/PopupCreate.vue'

export default {
  components: {
    DashboardProfile,
    DashboardTitle,
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
      isPopupProfile: false,
      isPopupVisible: false,
      items: [
        {
          id: 'Item 1',
          projectTitle: 'Logibug v1',
          projectVersion: 'Testing version 1',
          projectPlatform: 'Web',
          projectTesting: 'Manual',
        },
        {
          id: 'Item 2',
          projectTitle: 'Logibug v1',
          projectVersion: 'Testing version 1',
          projectPlatform: 'Mobile',
          projectTesting: 'Manual',
        },
      ],
    }
  },
  methods: {
    showPopup() {
      this.isPopupVisible = true
    },
    closePopup() {
      this.isPopupVisible = false
    },
    openPopup() {
      this.isPopupVisible = true
    },
    openProfile() {
      this.isPopupProfile = true
    },
    createProject(project) {
      console.log('run', project)
      // console.log(project))

      project.id = this.items.length + 1
      this.items.push(project)
    },
    tes() {
      console.log('testing')
    },
    async getProject() {
      try {
        const response = await this.$axios.$get('/projects')
        console.log(response)
        this.items = response
      } catch (e) {
        console.log(e)
      }
    },
  },
  mounted() {
    this.getProject()
  },
}
</script>
