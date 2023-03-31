<template>
    <div>
        <form class="max-w-md mx-auto">
            <div class="mb-4">
                <input id="name" v-model="name" type="text" placeholder="Name"
                    class="w-full p-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
            </div>
            <div class="mb-4">
                <input id="email" v-model="email" type="email" placeholder="Email"
                    class="w-full p-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
            </div>
            <div class="mb-4">
                <input id="password" v-model="password" type="password" placeholder="Password"
                    class="w-full p-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
            </div>
            <div class="mb-4">
                <input id="confirmPassword" v-model="confirmPassword" type="password" placeholder="Confirm Password"
                    class="w-full p-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
            </div>
            <div class="mb-8">
                <button type="submit"
                    class="w-full py-2 bg-blue-500 text-white rounded-md hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-500">
                    Register
                </button>
            </div>
        </form>
        <div class="text-center">
            <p class="text-gray-600">Already have an account? <nuxt-link to="/login"
                    class="text-blue-500 font-medium hover:underline">Login</nuxt-link></p>
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