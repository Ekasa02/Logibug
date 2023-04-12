<template>
    <div class="px-[100px] mt-[35px]">
        <div class="overflow-x-auto">
            <table class="table-auto w-full">
                <thead>
                    <tr class="bg-[#F8F8FA] text-[#1a1a1a] border border-solid border-gray-200">
                        <th class="px-4 py-2">Name</th>
                        <th class="px-4 py-2">Last Edited</th>
                        <th class="px-4 py-2">Created by</th>
                        <th class="px-4 py-2">Action</th>
                    </tr>
                </thead>
                <tbody>
                    <tr
                        v-for="(project, index) in displayedProjects" :key="index"
                        class="bg-white border-b border-solid border-gray-200">
                            <td class="px-4 py-2 text-center">{{ project.name }}</td>
                            <td class="px-4 py-2 text-center">{{ project.lastEdited }}</td>
                            <td class="px-4 py-2 text-center">{{ project.createdBy }}</td>
                            <td class="px-4 py-2 text-center"><button @click="deleteProject(project.id)">Delete</button></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="flex justify-end mt-4">
            <button
                class="px-4 py-2 border border-solid border-gray-300" :disabled="currentPage === 1"
                @click="currentPage--">
                <img
                    src="./svg/Previous.svg" alt="Next" height="14px" width="8px"
                    :style="{ filter: currentPage === lastPage ? 'invert(98%) sepia(1%) saturate(1149%) hue-rotate(252deg) brightness(114%) contrast(70%)' : '' }">
            </button>
            <div class="px-4 py-2 bg-white border border-solid border-gray-300 mx-[10px]">{{ currentPage }}</div>
            <button
                class="px-4 py-2 border border-solid border-gray-300" :disabled="currentPage === lastPage"
                @click="currentPage++">
                <img
                    src="./svg/Next.svg" alt="Next" height="14px" width="8px"
                    :style="{ filter: currentPage === lastPage ? 'invert(98%) sepia(1%) saturate(1149%) hue-rotate(252deg) brightness(114%) contrast(70%)' : '' }">
            </button>
        </div>
    </div>
</template>
  
<script>
export default {
    name: "TableComponent",
    props: {
        projects: {
            type: Array,
            required: true,
            default: () => []
        }
    },
    data() {
        return {
            currentPage: 1,
            projectsPerPage: 5
        };
    },
    computed: {
        displayedProjects() {
            const startIndex = (this.currentPage - 1) * this.projectsPerPage;
            const endIndex = startIndex + this.projectsPerPage;
            return this.projects.slice(startIndex, endIndex);
        },
        lastPage() {
            return Math.ceil(this.projects.length / this.projectsPerPage);
        }
    },
    methods: {
        deleteProject(projectId) {
            // Call delete API with projectId
        },
        previousPage() {
            if (this.currentPageIndex > 0) {
                this.currentPageIndex--;
            }
        },
        nextPage() {
            if (this.currentPageIndex < this.totalPages - 1) {
                this.currentPageIndex++;
            }
        }
    }
};
</script>

<style lang="scss" scoped></style>