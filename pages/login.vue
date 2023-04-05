<template>
  <div class="h-screen flex">
    <div class="w-2/5 px-[80px] py-[80px]">
      <LogibugLogo />
      <LoginTitle />
      <LoginForm />
    </div>
    <div class="w-3/5 bg-blue-500"></div>
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