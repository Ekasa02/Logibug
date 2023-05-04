<template>
  <div class="bg-[#33333385] fixed top-0 left-0 right-0 bottom-0 flex items-center sm:justify-center font-['monserrat']">
    <div>
      <div class="bg-white rounded-lg shadow-lg">
        <header-create></header-create>
        <div class="pl-5 pr-5">
          <scenario-test></scenario-test>
          <test-category></test-category>
          <pre-condition></pre-condition>
          <test-case></test-case>
          <test-step></test-step>
          <expect-test></expect-test>
          <div class="pt-6">
            <button-create></button-create>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ButtonCreate from '../createproject/ButtonCreate.vue';
import HeaderCreate from './HeaderCreate.vue';
import ScenarioTest from './ScenarioTest.vue';
import TestCategory from './TestCategory.vue';
import PreCondition from './PreCondition.vue';
import TestCase from './TestCase.vue';
import TestStep from './TestStep.vue';
import ExpectTest from './ExpectTest.vue';

export default {
  components: {
    HeaderCreate,
    ScenarioTest,
    TestCategory,
    PreCondition,
    TestCase,
    TestStep,
    ExpectTest,
    ButtonCreate,
  },
}
</script>
