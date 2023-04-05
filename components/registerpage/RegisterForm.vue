<template>
    <div class="mt-[30px]">
        <form class="max-w-md mx-auto">
            <div class="mb-5">
                <input id="name" v-model="name" type="text" placeholder="Name" class="w-full px-[16px] py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500
                        placeholder-gray-500 placeholder-opacity-50 placeholder-font-medium placeholder-text-sm
                        leading-[24px] text-[16px]">
            </div>
            <div class="mb-5">
                <input id="email" v-model="email" type="email" placeholder="Email" class="w-full px-[16px] py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500
                        placeholder-gray-500 placeholder-opacity-50 placeholder-font-medium placeholder-text-sm
                        leading-[24px] text-[16px]">
            </div>
            <div class="mb-5">
                <input id="password" v-model="password" type="password" placeholder="Password" class="w-full px-[16px] py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500
                        placeholder-gray-500 placeholder-opacity-50 placeholder-font-medium placeholder-text-sm
                        leading-[24px] text-[16px]">
            </div>
            <div class="mb-7">
                <input id="confirmPassword" v-model="confirmPassword" type="password" placeholder="Confirm Password" class="w-full px-[16px] py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500
                        placeholder-gray-500 placeholder-opacity-50 placeholder-font-medium placeholder-text-sm
                        leading-[24px] text-[16px]">
            </div>
            <div class="mb-6">
                <button type="submit"
                    class="w-full py-[10px] bg-[#554AF0] text-white rounded-[8px] text-md hover:bg-blue-600">
                    Register
                </button>
            </div>
        </form>
        <div class="text-center text-sm">
            <p class="text-[#333333]">Already have an account?
                <nuxt-link to="/login" class="text-[#333333] font-semibold font-sm hover:underline">Login
                </nuxt-link>
            </p>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: '',
            email: '',
            password: '',
            confirmPassword: ''
        }
    }
}
</script>

<style lang="scss" scoped></style>