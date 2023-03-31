<template>
    <div class="h-screen flex">
        <div class="w-1/3 p-8">
            <LogibugLogo />
            <RegisterTitle />
            <RegisterForm />
        </div>
        <div class="w-2/3 bg-blue-500"></div>
    </div>
</template>
  
<script>

import LogibugLogo from '../components/major/LogibugLogo.vue';
import RegisterForm from '../components/registerpage/RegisterForm.vue';
import RegisterTitle from '../components/registerpage/RegisterTitle.vue';

export default {
    components: {
        LogibugLogo,
        RegisterForm,
        RegisterTitle
    }
}
</script>
  
<style lang="scss" scoped></style>