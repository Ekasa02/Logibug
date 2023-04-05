<template>
    <div class="flex items-center justify-between px-[100px] py-[25px] bg-[#F8F8FA] border-b border-gray-300">
        <div class="flex items-center">
            <LogibugLogo />
            <NavbarList />
        </div>

        <div class="flex items-center space-x-[40px]">
            <NavbarLogin />
            <NavbarRegister />
        </div>
    </div>
</template>

<script>
import NavbarList from '../navbar/NavbarList.vue';
import NavbarLogin from '../navbar/NavbarLogin.vue';
import NavbarRegister from '../navbar/NavbarRegister.vue';
import LogibugLogo from './LogibugLogo.vue';

export default {
    components: { LogibugLogo, NavbarList, NavbarLogin, NavbarRegister }
}
</script>

<style lang="scss" scoped></style>