<template>
    <div  >
      <button class="rounded-full overflow-hidden" @click="openProfile">
        <img class="w-12 h-12  object-cover" :src="items.img_url" alt="Profile Picture">
      </button>
    </div>
</template>

<script>
export default{
  data(){
    return{
      items:[]
    }
  },
  mounted (){
      this.getProfile();
    },
    methods: {
    openProfile() {
      this.$emit('open')
    },
    async getProfile() {
            try {
                const response = await this.$axios.$get('/profiles')
                console.log(response)
                this.items = response.data
            } catch (e) {
                console.log(e)
            }
        }
  },
}
</script>

<style lang="scss" scoped></style>