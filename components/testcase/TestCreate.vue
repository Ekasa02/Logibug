<template>
    <div class="fixed inset-0 flex items-center justify-center">
        <div class="bg-white p-8 rounded-lg shadow-lg w-[35%] max-h-[80vh] overflow-hidden">
            <div class="flex justify-between">
                <h1 class="font-Montserrat font-bold text-2xl pr-12">Create test case</h1>
                <img src="../createversion/svg/CloseCircle.svg" class="cursor-pointer" @click="closeModal" alt="Close Icon">
            </div>
            <hr class="border-gray-300 my-4 w-full">
            <div class="overflow-y-auto max-h-[60vh] pr-5">
                <form @submit.prevent="postProject">
                    <div class="relative">
                        <label class="block font-['Montserrat'] font-bold text-[14px] mb-2" for="testcase">
                            Test case
                        </label>
                        <input id="testcase"
                            class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                            type="text" placeholder="Test case" v-model="newItem.testcase">
                    </div>
                    <div class="relative pt-[15px]">
                        <label class="block font-Montserrat font-bold text-[14px] mb-2" for="scenario">
                            Scenario
                        </label>
                        <div class="flex items-center">
                            <input id="scenario"
                                class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                                type="text" placeholder="Scenario" disabled />
                            <div
                                @click="showScenario"
                                class="hover:opacity-80 text-white font-bold py-2 px-2.5 rounded-xl ml-3 border border-gray-300">
                                <img src="./svg/Plus.svg" alt="Plus Icon" class="h-5 w-5">
                            </div>
                        </div>
                    </div>
                    <div class="pt-[15px] relative">
                        <label class="block font-['Montserrat'] font-bold text-[14px] mb-2" for="test-category">
                            Test category
                        </label>
                        <div class="flex items-center">
                            <select id="test-category"
                                class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                                v-model="newItem.test_category">
                                <option value="" disabled selected>Test category</option>
                                <option value="positif">Positive</option>
                                <option value="negatif">Negative</option>
                            </select>
                        </div>
                    </div>
                    <div class="pt-[15px] relative">
                        <label class="block font-['Montserrat'] font-bold text-[14px] mb-2" for="pre-condition">
                            Pre condition
                        </label>
                        <input id="pre-condition"
                            class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                            type="text" placeholder="Pre condition" v-model="newItem.pre_condition">
                    </div>
                    <div class="pt-[15px] relative">
                        <label class="block font-['Montserrat'] font-bold text-[14px] mb-2" for="test-step">
                            Test steps
                        </label>
                        <textarea id="test-step"
                            class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                            rows="4" placeholder="Steps" v-model="newItem.test_step">
                        </textarea>
                    </div>
                    <div class="pt-[15px] relative">
                        <label class="block font-['Montserrat'] font-bold text-[14px] mb-2" for="expectation">
                            Expectation
                        </label>
                        <input id="expectation"
                            class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                            type="text" placeholder="Expectation" v-model="newItem.expectation">
                    </div>
                    <div class="pt-[50px]">
                        <button class="font-['Montserrat'] bg-[#554AF0] text-white font-bold py-2 px-4 rounded"
                            type="submit">
                            Create
                        </button>
                    </div>
                </form>
            </div>
        </div>
        <TestScenario v-if="isScenarioVisible" :id="id" @hideScenario="hideScenario"/>
    </div>
</template>

<script>
import TestScenario from './TestScenario.vue';
export default {
    components: { TestScenario },
    props: {
        id: {
            type: String,
            required: true
        },
        scenarioId: {
            type: Number,
            required: true
        }
    },
    data() {
        return {
            isScenarioVisible: false,
            newItem: {
                scenario_id: '',
                version_id: '',
                testcase: '',
                test_category: '',
                pre_condition: '',
                test_step: '',
                expectation: ''
            }
        };
    },
    methods: {
        showScenario() {
            this.isScenarioVisible = true;
        },
        hideScenario() {
            this.isScenarioVisible = false;
        },     
        closeModal() {
            this.$emit("hideCreate");
        },
        async postProject() {
            this.newItem.scenario_id = this.scenarioId;
            this.newItem.version_id = this.id;
            console.log(this.newItem); // Log newItem object
            try {
                const response = await this.$axios.$post('/test_cases', this.newItem);
                console.log(response);
                // Handle the response, show success message, etc.
            } catch (error) {
                console.log(error);
                // Handle the error, show error message, etc.
            }
            // Reset form fields
            this.newItem = {
                scenario_id: '',
                version_id: '',
                testcase: '',
                test_category: '',
                pre_condition: '',
                test_step: '',
                expectation: ''
            };
        }
    }
};
</script>

