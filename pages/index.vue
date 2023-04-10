<template>
  <div>
    <LogibugNavbar />
    <LogibugTest />
  </div>
</template>

<script>
import LogibugNavbar from '../components/major/LogibugNavbar.vue';
import LogibugTest from '../components/major/LogibugJumbotron.vue';

export default {
  components: {
    LogibugNavbar,
    LogibugTest
  }
}
</script>

<style lang="scss" scoped></style>