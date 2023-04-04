<template>
  <div class="h-screen flex">
    <div class="w-1/3 p-8">
      <LogibugLogo />
      <LoginTitle />
      <LoginForm />
    </div>
    <div class="w-2/3 bg-blue-500"></div>
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