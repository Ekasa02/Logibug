<template>
    <div>
      <text-page></text-page>
      <div class="container ">
        <div class="flex ">
          <div >
            <text-page></text-page>
          </div>
          <image-content></image-content>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import ImageContent from '../components/landingpage/ImageContent.vue';
//   import TextBox from '../components/landingpage/TextBox.vue';
  import TextPage from '../components/landingpage/TextPage.vue';
  
  export default {
    components: {
      ImageContent,
    //   TextBox,
      TextPage,
    },
  };
  </script>
  