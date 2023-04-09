<template>
    <div class="mt-[30px]">
        <form class="max-w-md mx-auto">
            <div class="relative mb-4">
                <input id="name" v-model="name" type="text"
                    class="block px-12 py-2 w-full text-gray-900 bg-transparent rounded-lg border border-solid border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-blue-600 peer"
                    placeholder=" " />
                <label for="name"
                    class="absolute text-[#4D4D4D] font-medium duration-300 transform -translate-y-4 scale-75 top-2 origin-[0] bg-white px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-focus:-top-1 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:scale-75 peer-focus:-translate-y-2 left-10">Name</label>
                <img src="../icons/User.svg" alt="Mail Icon" class="absolute left-3 top-2.5 h-5 w-5">
            </div>
            <div class="relative mb-4">
                <input id="email" v-model="email" type="email"
                    class="block px-12 py-2 w-full text-gray-900 bg-transparent rounded-lg border border-solid border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-blue-600 peer"
                    placeholder=" " />
                <label for="email"
                    class="absolute text-[#4D4D4D] font-medium duration-300 transform -translate-y-4 scale-75 top-2 origin-[0] bg-white px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-focus:-top-1 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:scale-75 peer-focus:-translate-y-2 left-10">Email</label>
                <img src="../icons/Mail.svg" alt="Mail Icon" class="absolute left-3 top-2.5 h-5 w-5">
            </div>
            <div class="relative mb-4">
                <input id="password" v-model="password" type="password"
                    class="block px-12 py-2 w-full text-gray-900 bg-transparent rounded-lg border border-solid border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-blue-600 peer"
                    placeholder=" " />
                <label for="email"
                    class="absolute text-[#4D4D4D] font-medium duration-300 transform -translate-y-4 scale-75 top-2 origin-[0] bg-white px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-focus:-top-1 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:scale-75 peer-focus:-translate-y-2 left-10">Password</label>
                <img src="../icons/Password.svg" alt="Lock Icon" class="absolute left-3 top-2.5 h-5 w-5">
            </div>
            <div class="relative mb-7">
                <input id="confirmPassword" v-model="confirmPassword" type="password"
                    class="block px-12 py-2 w-full text-gray-900 bg-transparent rounded-lg border border-solid border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-blue-600 peer"
                    placeholder=" " />
                <label for="email"
                    class="absolute text-[#4D4D4D] font-medium duration-300 transform -translate-y-4 scale-75 top-2 origin-[0] bg-white px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-focus:-top-1 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:scale-75 peer-focus:-translate-y-2 left-10">Confirm Password</label>
                <img src="../icons/Password.svg" alt="Lock Icon" class="absolute left-3 top-2.5 h-5 w-5">
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
                <nuxt-link to="/login" class="text-[#554AF0] font-semibold font-sm hover:underline">Login
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