<template>
    <div>
        <h1 class="text-2xl font-bold">Hello, {{ userName }}</h1>
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