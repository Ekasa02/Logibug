<template>
    <div>
        <button @click="logout">Logout</button>
    </div>
</template>

<script>
    export default {
        methods: {
        async logout() {
            await this.$auth.logout(/* .... */)
        }
    }
} 
    
</script>

<style lang="scss" scoped>
    
</style>