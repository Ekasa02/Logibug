<template>
    <div>
        <form class="max-w-md mx-auto">
            <div class="mb-4">
                <input id="email"  type="email" placeholder="Email" class="w-full p-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
            </div>
           
            <div class="mb-8">
                <button type="submit" class="w-full py-2 bg-blue-500 text-white rounded-md hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-500">
                    Send
                </button>
            </div>
        </form>
        <div class="text-center">
            <p class="text-gray-600">Don't have an account? <a href="#" class="text-blue-500 font-medium hover:underline">Register</a></p>
        </div>
    </div>
</template>
  
<script>
export default {
    data() {
        return {
            email: ''
        }
    }
}
</script>

<style lang="scss" scoped></style>