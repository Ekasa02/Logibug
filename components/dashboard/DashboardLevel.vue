<template>
    <div
        :class="`rounded-[28px] px-6 py-2 w-[120px] flex items-center justify-center mt-3 text-white font-semibold text-sm ${levelClass}`">{{ level }}</div>
</template>
  
<script>
export default {
    props: {
        level: {
            type: String,
            required: true
        }
    },
    computed: {
        levelClass() {
            switch (this.level) {
                case 'Beginner':
                    return 'bg-[#DD00D2]';
                case 'Intermediate':
                    return 'bg-yellow-500';
                case 'Advanced':
                    return 'bg-red-500';
                default:
                    return 'bg-[#DD00D2]';
            }
        }
    }
}
</script>
  