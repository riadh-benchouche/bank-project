<script setup lang="ts">
// @ts-ignore
import  * as styles  from "../styles.js";

const props = defineProps({
  feature: {
    type: Object,
    required: false,
    default: {},
  },
  index: {
    type: String,
    required: false,
    default: '',
  },
})
</script>

<template>
  <div :class="`flex flex-row p-6 rounded-[20px] ${props.index !== 'feature-3' ? 'mb-6' : 'mb-0'} feature-card`">
    <div :class="`w-[64px] h-[64px] rounded-full  bg-dimBlue ${styles.flexCenter}`">
      <img :src=props.feature.icon alt="star" class="w-[50%] h-[50%] object-contain"/>
    </div>
    <div class="flex-1 flex flex-col ml-3">
      <h4 class="font-poppins font-semibold text-white text-[18px] leading-[23.4px] mb-1">
        {{ props.feature.title }}
      </h4>
      <p class="font-poppins font-normal text-dimWhite text-[16px] leading-[24px]">
        {{ props.feature.content }}
      </p>
    </div>
  </div>
</template>

<style scoped>
</style>
