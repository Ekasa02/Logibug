<template>
  <div
    class="bg-[#33333385] fixed top-16  right-0 transform -translate-x-28"
  >
    <div class="w-450px h-540px">
      <div class="bg-white rounded-lg shadow-lg">
        <header-account></header-account>
        <div class="pl-5">
          <account-profil></account-profil>
        </div>
        <level-app></level-app>
      </div>
    </div>
  </div>
</template>

<script>
import HeaderAccount from '../profil/HeaderAccount.vue'
import AccountProfil from '../profil/AccountProfil.vue'
import LevelApp from '../profil/LevelApp.vue'

export default {
  components: {
    HeaderAccount,
    AccountProfil,
    LevelApp,
  },
}
</script>

<style>

</style>
