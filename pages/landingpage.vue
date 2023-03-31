<template>
    <div>
        <text-page> </text-page>
        <image-content></image-content>
        
    </div>
   
</template>

<script>
    import ImageContent from '../components/landingpage/ImageContent.vue';
    import TextPage from '../components/landingpage/TextPage.vue';
    
export default{
    components:{
        ImageContent,
        TextPage,
    }
}
</script>