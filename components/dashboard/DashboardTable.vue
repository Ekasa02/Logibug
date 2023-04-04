<template>
    <div class="overflow-x-auto">
        <table class="table-auto w-full">
            <thead>
                <tr class="bg-blue-800 text-white">
                    <th class="px-4 py-2">Name</th>
                    <th class="px-4 py-2">Last Edited</th>
                    <th class="px-4 py-2">Created by</th>
                    <th class="px-4 py-2">Action</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(project, index) in projects" :key="index"
                    :class="(index % 2 === 0) ? 'bg-gray-200' : 'bg-gray-300'">
                    <td class="px-4 py-2 text-center">{{ project.name }}</td>
                    <td class="px-4 py-2 text-center">{{ project.lastEdited }}</td>
                    <td class="px-4 py-2 text-center">{{ project.createdBy }}</td>
                    <td class="px-4 py-2 text-center"><button @click="deleteProject(project.id)">Delete</button></td>
                </tr>
            </tbody>
        </table>
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
    methods: {
        deleteProject(projectId) {
            // Call delete API with projectId
        },
    },
};
</script>

<style lang="scss" scoped></style>