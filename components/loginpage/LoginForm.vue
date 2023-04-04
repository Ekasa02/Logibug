<template>
    <div>
        <form class="max-w-md mx-auto" @submit.prevent="login">
            <div class="mb-4">
                <input id="email" v-model="email" type="email" placeholder="Email"
                    class="w-full p-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
            </div>
            <div class="mb-4">
                <input id="password" v-model="password" type="password" placeholder="Password"
                    class="w-full p-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
                <a href="#" class="text-blue-500 text-sm font-medium float-right hover:underline">Forgot password?</a>
            </div>
            <div class="mb-8">
                <button type="submit"
                    class="w-full py-2 bg-blue-500 text-white rounded-md hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-500">
                    Login
                </button>
            </div>
        </form>
        <div class="text-center">
            <p class="text-gray-600">Don't have an account? <nuxt-link to="/register"
                    class="text-blue-500 font-medium hover:underline">Register</nuxt-link></p>
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