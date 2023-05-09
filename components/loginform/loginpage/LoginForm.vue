<template>
    <div class="mt-[30px]">
        <form class="max-w-md" @submit.prevent="userLogin">
            <div class="relative mb-4">
                <input id="email" v-model="userInfo.email" type="email"
                    class="block px-12 py-2 w-full text-gray-900 bg-transparent rounded-lg border border-solid border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-blue-600 peer"
                    placeholder=" " />
                <label for="email"
                    class="absolute text-[#4D4D4D] font-medium duration-300 transform -translate-y-4 scale-75 top-2 origin-[0] bg-white px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-focus:-top-1 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:scale-75 peer-focus:-translate-y-2 left-10">Email</label>
                <img src="../svg/Mail.svg" alt="Mail Icon" class="absolute left-3 top-2.5 h-5 w-5">
            </div>
            <div class="mb-4 relative">
                <input id="password" v-model="userInfo.password" :type="showPassword ? 'text' : 'password'"
                    class="block px-12 py-2 w-full text-gray-900 bg-transparent rounded-lg border border-solid border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-blue-600 peer"
                    placeholder=" " />
                <label for="password"
                    class="absolute text-[#4D4D4D] font-medium duration-300 transform -translate-y-4 scale-75 top-2 origin-[0] bg-white px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-focus:-top-1 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:scale-75 peer-focus:-translate-y-2 left-10">Password</label>
                <img src="../svg/Password.svg" at="Lock Icon" class="absolute left-3 top-2.5 h-5 w-5" />
                <img src="../svg/ShowPassword.svg" alt="Show Password Icon"
                    class="absolute right-3 top-2.5 h-5 w-5 cursor-pointer" @click="showPassword = !showPassword" />
            </div>
            <div class="mb-6">
                <button class="w-full py-[10px] bg-[#554AF0] text-white rounded-[8px] text-md hover:bg-blue-600"
                    type="submit">
                    Log in
                </button>
            </div>
        </form>
        <div class="text-center text-sm">
            <p class="text-[#333333]">
                Don't have an account?
                <nuxt-link to="/register" class="text-[#554AF0] font-semibold font-sm hover:underline">
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
            userInfo: {
                email: "asharimidana1@gmail.com",
                password: "12345678",
            },  
            showPassword: false,
        };
    },
    methods: {
        async userLogin() {
            try {
                const response = await this.$auth.loginWith('local', { data: this.userInfo })
                console.log(response)
                this.$router.push('/dashboard')
            } catch (err) {
                console.log(err)
            }
        }
    }
}
</script>

<style lang="scss" scoped></style>