<template>
  <div
    class="bg-[#33333385] fixed top-0 left-0 right-0 bottom-0 flex items-center sm:justify-center"
  >
    <div>
      <div class="bg-white rounded-lg shadow-lg">
          <header-project></header-project>
          <div class="pl-5 pr-5">
            <project-name></project-name>
            <!-- <desc-project></desc-project> -->
            <testing-type></testing-type>
            <drop-platform></drop-platform>
        </div>
        <div class="flex pt-[60px] justify-between pr-5 pb-6">
          <button-cancel class="ml-auto mr-[15px]"></button-cancel>
          <button-save></button-save>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ButtonCancel from '../createproject/ButtonCancel.vue'
import HeaderProject from '../editproject/HeaderProject.vue'
import ProjectName from '../createproject/ProjectName.vue'
// import DescProject from '../createproject/DescProject.vue'
import TestingType from '../createproject/TestingType.vue'
import DropPlatform from '../createproject/DropPlatform.vue'
import ButtonSave from './ButtonSave.vue'

export default {
  components: {
    ButtonCancel,
    ButtonSave,
    HeaderProject,
    ProjectName,
    // DescProject,
    TestingType,
    DropPlatform,
  },
}
</script>
