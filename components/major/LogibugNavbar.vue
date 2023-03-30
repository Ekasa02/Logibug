<template>
    <div class="flex items-center justify-between px-6 py-4 bg-white shadow-md">
        <div class="flex items-center">
            <LogibugLogo />
        </div>

        <div class="flex items-center space-x-4">
            <NavbarList />
            <NavbarLogin />
        </div>
    </div>
</template>
  

<script>
import NavbarList from '../navbar/NavbarList.vue';
import NavbarLogin from '../navbar/NavbarLogin.vue';
import LogibugLogo from './LogibugLogo.vue';

export default {
    components: { LogibugLogo, NavbarList, NavbarLogin }
}
</script>

<style lang="scss" scoped></style>