<template>
    <div class="mt-[40px]">
        <h1 class="text-[#1a1a1a] text-xl md:text-4xl font-normal md:font-medium">Hello, <span class="font-bold">{{ userName }}</span></h1>
    </div>
</template>
  
<script>
export default {
    name: 'HelloUser',
    props: {
        userName: {
            type: String,
            required: true
        }
    }
}
</script>

<style lang="scss" scoped></style>