<template>
    <div  >
      <button class="rounded-full overflow-hidden" @click="openProfile">
        <img class="w-12 h-12  object-cover" src="./svgs/User.svg" alt="Profile Picture">
      </button>
    </div>
</template>

<script>
export default{
    methods: {
    openProfile() {
      this.$emit('open')
    },
  },
}
</script>

<style lang="scss" scoped></style>