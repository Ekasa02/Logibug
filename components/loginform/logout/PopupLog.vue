<template>
    <div class="bg-[#33333385] fixed top-0 left-0 right-0 bottom-0 flex sm:items-center sm:justify-center ">
        <div class="w-950px h-950px bg-white p-8 rounded-lg shadow-lg">
            <div class="pl-[400px]">
                <img src="../.././assets/CloseCircle.svg" alt="image" >
            </div>
            <div class="sm:pt-6 sm:pl-11 sm:pr-7">
                <img src="../../assets/Logout logo.svg" alt="image">
                <h1 class="text-center pt-7 font-['Montserrat'] font-bold">Logout Account?</h1>
                <p class="text-center  font-['Montserrat']">Are you sure you want to logout the account</p>
            </div>
            <div class="flex pt-[30px] sm:justify-center sm:items-center ">
                <button-no class=" mr-[19px]"></button-no>
                <button-yes></button-yes>
            </div>
        </div>
    </div>
</template>

<script>
import ButtonNo from "./ButtonNo.vue";
import ButtonYes from './ButtonYes.vue';

export default {
    components:{
        ButtonNo, 
        ButtonYes,
    }
}
</script>