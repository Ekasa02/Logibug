<template>
  <div class="h-screen flex">
    <div class="md:w-2/5 px-[30px] py-[30px] lg:px-[60px] flex items-center justify-items-center">
      <div class="margin-x-auto">
        <LogibugLogo />
        <LoginTitle />
        <LoginForm />
      </div>
    </div>
    <div class="hidden md:block w-3/5 bg-blue-500"></div>
  </div>
</template>
  
<script>
import LoginTitle from '../components/loginpage/LoginTitle.vue';
import LoginForm from '../components/loginpage/LoginForm.vue';
import LogibugLogo from '../components/major/LogibugLogo.vue';

export default {
  components: {
    LogibugLogo,
    LoginTitle,
    LoginForm,
  }
}
</script>
  
<style lang="scss" scoped></style>