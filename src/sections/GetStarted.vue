<script setup lang="ts">
// @ts-ignore
import styles from '../styles.js'
// @ts-ignore
import {arrowUp} from "../assets/index.js";

</script>

<template>
  <div :class="`${styles.flexCenter}`"
       class="w-[140px] h-[140px] rounded-full bg-blue-gradient p-[2px] cursor-pointer">
    <div :class="`${styles.flexCenter}`"
         class="flex-col w-[100%] h-[100%] rounded-full bg-primary cursor-pointer">
      <div :class="`${styles.flexStart}`"
           class="flex-row">
        <p class="font-poppins font-medium text-[18px] leading-[23px] mr-2.5">
          <span class="text-gradient">Get</span>
        </p>
        <img :src="arrowUp" alt="arrow" class="w-[23px] h-[23px] object-contain">
      </div>
      <p class="font-poppins font-medium text-[18px] leading-[23px]">
        <span class="text-gradient">Started</span>
      </p>
    </div>
  </div>
</template>

<style scoped>
</style>
