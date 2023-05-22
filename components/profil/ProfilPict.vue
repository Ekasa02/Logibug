<template>
    <div>
        <div>
            <h1 class=" font-bold text-[16px] leading-6 pt-8">Profile picture</h1>
        </div>
        <div class="flex">
            <div class="pt-4">
                <img :src="src" class="w-[200px] h-[200px] pt-3 rounded-full" alt="Profile picture">
            </div>
            <div class="pl-16 pt-10">
                <p>Maximum photo size is 1 MB</p>
                <button-select @click="browse"></button-select>
            </div>
        </div>
       
    </div>
</template>

<script>
import ButtonSelect from "../profil/ButtonSelect.vue"

export default {
    props:{
        value:{
            type:Object,
            default:null
        },
        defaultSrc:String
    },
    data(){
        return{
            src:null,
            file:null,
        };
    },
    methods:{
        browse(){
            this.$refs.file.click();
        },
        change(e){
            this.file=e.target.files[0];
            this.$emit("input", this.file);
            const reader = new FileReader();
            reader.readAsDataURL(e.target.files[0]);
            reader.onload = (e) => {
                this.src = e.target.result;
            }
        },
        // openFile(){
        //     const input = document.createElement('input');
        //     input.type='file';
        //     input.accept='image/*';
        //     input.onchange=this.handleFileSelect;
        //     input.click();
        // },
        // handleFileSelect(event){
            
        //     const file = event.target.files[0];
        //     this.uploadImage(file); 
        // },
        // uploadImage(file){
        //     const formData = new FormData();
        //     formData.append('image',file);
        //     fetch('http://localhost:3000/api/v1/profiles',{
        //         method:'GET',
        //         body:formData,
        //     })
        //     .then(response=>{
        //         console.log(JSON.stringify(response.formData));
        //     })
        //     .catch(error=>{
        //         console.log(error);
        //     });
        // }
    },
    components:{
        ButtonSelect,
    }
}
</script>
