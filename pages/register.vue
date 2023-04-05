<template>
    <div class="h-screen flex">
        <div class="w-2/5 px-[80px] py-[40px]">
            <LogibugLogo />
            <RegisterTitle />
            <RegisterForm />
            <RegisterTerms />
        </div>
        <div class="w-3/5 bg-blue-500"></div>
    </div>
</template>
  
<script>

import LogibugLogo from '../components/major/LogibugLogo.vue';
import RegisterForm from '../components/registerpage/RegisterForm.vue';
import RegisterTitle from '../components/registerpage/RegisterTitle.vue';
import RegisterTerms from '../components/registerpage/RegisterTerms.vue';

export default {
    components: {
        LogibugLogo,
        RegisterForm,
        RegisterTitle,
        RegisterTerms
    }
}
</script>
  
<style lang="scss" scoped></style>