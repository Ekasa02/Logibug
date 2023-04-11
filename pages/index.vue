<template>
  <div class="w-100% overflow-x-hidden">
    <LogibugNavbar />
    <LogibugTest />
    <AboutPage />
    <VersionPage />
    <FooterPage />
  </div>
</template>

<script>
import LogibugNavbar from '../components/major/LogibugNavbar.vue';
import LogibugTest from '../components/major/LogibugJumbotron.vue';
import AboutPage from '../components/landingpage/AboutPage.vue';
import VersionPage from '../components/landingpage/VersionPage.vue';
import FooterPage from '../components/landingpage/FooterPage.vue';

export default {
  components: {
    LogibugNavbar,
    LogibugTest,
    AboutPage,
    VersionPage,
    FooterPage
  }
}
</script>

<style lang="scss" scoped></style>