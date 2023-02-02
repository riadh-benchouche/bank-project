<script setup lang="ts">
const props = defineProps({
  styles: String,
  msg: String
})
</script>

<template>
  <div>
    <button type="button"
            :class="`py-4 px-6 font-poppins font-medium text-[18px] text-primary bg-blue-gradient rounded-[10px] outline-none ${props.styles}`">
      {{ props.msg }}
    </button>
  </div>
</template>

<style scoped>
</style>
