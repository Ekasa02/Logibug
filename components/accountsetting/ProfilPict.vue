<template>
    <div>
        <div>
            <h1 class=" font-bold text-[16px] leading-6 pt-4">Profile picture</h1>
        </div>
        <div class="flex items-center gap-x-12">
            <div class="">
                <img src=".././assets/Profil.svg" class="w-[125px] h-[125px] pt-3 rounded-full" alt="Profile picture">
            </div>
            <div class="">
                <p>Maximum photo size is 1 MB</p>
                <button-select></button-select>
            </div>
        </div>
       
    </div>
</template>

<script>
import ButtonSelect from "../profil/ButtonSelect.vue"

export default {
    components:{
        ButtonSelect,
    }
}
</script>
