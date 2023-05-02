<template>
    <div class="bg-[#33333385] fixed top-0 left-0 right-0 bottom-0 flex items-center justify-center ">
        <div class="w-950px h-950px bg-white p-8 rounded-lg shadow-lg">
            <div>
                <header-project></header-project>
            </div>
            <div>
                <project-name></project-name>
            </div>
            <div>
                <desc-project></desc-project>
            </div>
            <div class="flex pt-[70px] justify-between ">
                <button-cancel class="ml-auto mr-[15px]"></button-cancel>
                <button-create></button-create>
            </div>

        </div>
    </div>
</template>

<script>
import ButtonCancel from '../createproject/ButtonCancel.vue';
import ButtonCreate from '../createproject/ButtonCreate.vue';
import HeaderProject from '../createproject/HeaderProject.vue';
import ProjectName from '../createproject/ProjectName.vue';
import DescProject from '../createproject/DescProject.vue';

export default {
    components: {
        ButtonCancel,
        ButtonCreate,
        HeaderProject,
        ProjectName,
        DescProject
    }
}
</script>