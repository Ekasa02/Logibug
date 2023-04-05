<template>
    <div class="mt-[60px]">
        <form class="max-w-md" @submit.prevent="login">
            <div class="mb-4">
                <input id="email" v-model="email" type="email" placeholder="Email" class="w-full px-[16px] py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500
                              placeholder-gray-500 placeholder-opacity-50 placeholder-font-medium placeholder-text-sm
                              leading-[24px] text-[16px]">
            </div>
            <div class="mb-4">
                <input id="password" v-model="password" type="password" placeholder="Password" class="w-full px-[16px] py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500
                              placeholder-gray-500 placeholder-opacity-50 placeholder-font-medium placeholder-text-sm
                              leading-[24px] text-[16px]">
                <a href="#" class="mt-[10px] mb-8 text-[#686777] text-sm font-medium float-right hover:underline">Forgot
                    password?</a>
            </div>
            <div class="mb-6">
                <button type="submit" class="w-full py-[10px] bg-[#554AF0] text-white rounded-[8px] text-md hover:bg-blue-600">
                    Log in
                </button>
            </div>
        </form>
        <div class="text-center text-sm">
            <p class="text-[#333333]">
                Don't have an account?
                <nuxt-link to="/register" class="text-[#333333] font-semibold font-sm hover:underline">
                    Register
                </nuxt-link>
            </p>
        </div>
    </div>
</template>
  
<script>
export default {
    data() {
        return {
            email: '',
            password: ''
        }
    },
    methods: {
        login() {
            this.$router.push('/dashboard')
        }
    }
}
</script>

<style lang="scss" scoped></style>