<template>
  <div >
    <LogibugNavbar />
    <LogibugTest />
    <AboutPage/>
    <version-page></version-page>
    <footer-page></footer-page>
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