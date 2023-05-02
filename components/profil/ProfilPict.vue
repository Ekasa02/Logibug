<template>
    <div>
        <div>
            <h1 class=" font-bold text-[16px] leading-6 pt-8">Profile picture</h1>
        </div>
        <div class="flex">
            <div class="pt-4">
                <img src=".././assets/Profil.svg" class="w-[200px] h-[200px] pt-3 rounded-full" alt="Profile picture">
            </div>
            <div class="pl-16 pt-10">
                <p>Maximum photo size is 1 MB</p>
                <button-select></button-select>
            </div>
        </div>
       
    </div>
</template>

<script>
import ButtonSelect from "./ButtonSelect.vue"

export default {
    components:{
        ButtonSelect,
    }
}
</script>
