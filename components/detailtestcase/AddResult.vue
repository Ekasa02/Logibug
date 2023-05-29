<template>
  <div>
    <div class="bg-white w-[75%] min-h-[60vh] rounded-lg shadow-lg px-8 py-8 float-right mt-5">
      <div class="ml-auto">
        <h1 class="font-bold text-2xl">Result</h1>
        <p class="pt-3 text-sm text-[#6A6D71]">Not result yet</p>
        <div class="pt-2">
          <button class="font-montserrat w-[100%] bg-[#554AF0] text-white font-bold py-2 px-4 rounded" @click="showCreate">
            Add result
          </button>
        </div>
      </div>
    </div>
    <CreateResult v-if="isCreateVisible" :id="id" @hideCreate="hideCreate"/>
  </div>
</template>
  
<script>
import CreateResult from './CreateResult.vue';
export default {
  components: {
    CreateResult
  },
  props: {
    id: {
      type: Number,
      required: true
    }
  },
  data() {
    return {
      isCreateVisible: false,
    }
  },
  methods: {
    showCreate() {
      this.isCreateVisible = true
    },
    hideCreate() {
      this.isCreateVisible = false
    }
  }
}
</script>