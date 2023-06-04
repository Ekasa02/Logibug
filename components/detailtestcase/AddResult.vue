<template>
  <div>
    <div v-if="items.length === 0" class="bg-white w-[75%] min-h-[60vh] rounded-lg shadow-lg px-8 py-8 float-right mt-5">
      <div class="ml-auto">
        <h1 class="font-bold text-2xl">Result</h1>
        <p class="pt-3 text-sm text-[#6A6D71]">Not result yet</p>
        <div class="pt-2">
          <button class="font-montserrat w-[100%] bg-[#554AF0] text-white font-bold py-2 px-4 rounded"
            @click="showCreate">
            Add result
          </button>
        </div>
      </div>
    </div>
    <div v-else>
      <!-- Display response data here -->
      <div class="rounded-[20px] border border-[#B3B3B3] px-[40px] py-[20px] overflow-y-auto max-h-[65vh]">
        <div class="flex justify-between items-center">
          <h1 class="font-bold text-2xl">Result</h1>
          <img src="./svg/Edit.svg" class="h-[18px] w-[18px]" alt="">
        </div>
        <div v-for="item in items" :key="item.id">
          <!-- <h1 class="mt-4 font-semibold text-xl">Tester</h1> -->
          <h1 class="mt-4 font-semibold text-xl">Actually</h1>
          <h1>{{ item.bug }}</h1>
          <h1 class="mt-4 font-semibold text-xl">Status</h1>
          <div class="flex gap-x-3 text-white">
            <div class="px-[32.5px] py-[2px] bg-red-600 rounded-lg">
              <p>{{ item.status }}</p>
            </div>
            <div class="px-[32.5px] py-[2px] bg-[#FFB366] rounded-lg">
              <p>{{ item.priority }}</p>
            </div>
            <div class="px-[32.5px] py-[2px] bg-[#B600C9] rounded-lg">
              <p>{{ item.severity }}</p>
            </div>           
          </div>
          <h1 class="mt-4 font-semibold text-xl">Note</h1>
          <p>{{ item.note }}</p>
          <h1 class="mt-4 font-semibold text-xl">Attachment</h1>
          <img :src="item.img_url" alt="">
        </div>
      </div>
    </div>
    <CreateResult v-if="isCreateVisible" :id="id" @hideCreate="hideCreate" />
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
      items: [] // Initialize an empty array to hold the response data
    };
  },
  mounted() {
    this.getTestresult();
  },
  methods: {
    showCreate() {
      this.isCreateVisible = true;
    },
    hideCreate() {
      this.isCreateVisible = false;
    },
    getTestresult() {
      try {
        // Simulating the response data
        const response = {
          bug: "bug",
          id: 9,
          img_url: "http://res.cloudinary.com/dzirffrnn/image/upload/v1685345047/1_result.png",
          note: "coba",
          priority: "low",
          severity: "minor",
          status: "fail",
          test_case_id: 45
        };

        console.log(response);

        // Insert the response data into the items array
        this.items.push(response);
      } catch (error) {
        console.log(error);
      }
    }
  }
};
</script>
