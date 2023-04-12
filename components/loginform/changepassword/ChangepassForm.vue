<template>
    <div class="mt-[60px]">
        <form class="max-w-md ">       
            <div class="relative mb-4">
                <input id="password"  type="password" placeholder="New Password" class="block px-12 py-2 w-full text-gray-900 bg-transparent rounded-lg border border-solid border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-blue-600 peer">
                    <label for="email" class="absolute text-[#4D4D4D] font-medium duration-300 transform -translate-y-4 scale-75 top-2 origin-[0] bg-white px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-focus:-top-1 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:scale-75 peer-focus:-translate-y-2 left-10">
                        New Password
                    </label>
                    <img src="../icons/Password.svg" alt="Lock Icon" class="absolute left-3 top-2.5 h-5 w-5">   
            </div>
            <div class="relative mb-4">
                <input id="password"  type="password" placeholder="Confirm New Password" class="block px-12 py-2 w-full text-gray-900 bg-transparent rounded-lg border border-solid border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-blue-600 peer">
                    <label for="email" class="absolute text-[#4D4D4D] font-medium duration-300 transform -translate-y-4 scale-75 top-2 origin-[0] bg-white px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-focus:-top-1 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:scale-75 peer-focus:-translate-y-2 left-10">
                        Confirm New Password
                    </label>
                    <img src="../icons/Password.svg" alt="Lock Icon" class="absolute left-3 top-2.5 h-5 w-5">    
            </div>
        </form>
        <div class="mb-6 pt-6">
            <button type="submit" class="w-full py-[10px] bg-[#554AF0] text-white rounded-[8px] text-md hover:bg-blue-600">
                Save
            </button>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            password: '',
            confirmPassword: ''
        }
    }
}
</script>

<style lang="scss" scoped></style>