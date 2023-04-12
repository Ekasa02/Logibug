<template>
    <div class="bg-[#33333385] fixed top-0 left-0 right-0 bottom-0 flex items-center justify-center ">
        <div class="w-950px h-950px bg-white p-8 rounded-lg shadow-lg">
            <div class="pl-[360px]">
                <img src="../popup/svg/CloseCircle.svg" alt="image" >
            </div>
            <div class="pt-6 pl-11 pr-7">
                <img src="../assets/Delete.svg" alt="image">
                <p class="text-center pt-7 font-['Montserrat'] text-[20px]">Are you sure to delete project</p>
                <h1 class="text-center font-['Montserrat'] font-bold">Project</h1>
            </div>
            <div class="flex pt-[30px] justify-between ">
                <button-cancel class="ml-auto mr-[15px]"></button-cancel>
                <button-delete></button-delete>
            </div>
        </div>
    </div>
</template>

<script>
import ButtonCancel from "../createproject/ButtonCancel.vue";
import ButtonDelete from './ButtonDelete.vue';

export default {
    components:{
        ButtonCancel, 
        ButtonDelete
    }
}
</script>