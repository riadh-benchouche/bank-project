<script setup lang="ts">
// @ts-ignore
import {quotes} from "../assets/index.js";

const props = defineProps({
  feedback: {
    type: Object,
    required: false,
    default: {}
  },
  index: {
    type: String,
    required: false,
    default: ''
  },
})
</script>

<template>
  <div
      class="flex justify-between flex-col px-10 py-12 rounded-[20px]  max-w-[370px] md:mr-10 sm:mr-5 mr-0 my-5 feedback-card">
    <img :src="quotes" alt="double_quotes" class="w-[42.6px] h-[27.6px] object-contain"/>
    <p class="font-poppins font-normal text-[18px] leading-[32.4px] text-white my-10">
      {{ props.feedback.content }}
    </p>

    <div class="flex flex-row">
      <img :src="props.feedback.img" alt={name} class="w-[48px] h-[48px] rounded-full"/>
      <div class="flex flex-col ml-4">
        <h4 class="font-poppins font-semibold text-[20px] leading-[32px] text-white">
          {{ props.feedback.name }}
        </h4>
        <p class="font-poppins font-normal text-[16px] leading-[24px] text-dimWhite">
          {{ props.feedback.title }}
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>
