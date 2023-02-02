<script setup lang="ts">
// @ts-ignore
import styles from '../styles.js'
// @ts-ignore
import {discount, robot} from "../assets/index.js";
// @ts-ignore
import GetStarted from "./GetStarted.vue";
</script>

<template>
  <section id="0" :class="`${styles.paddingY} flex md:flex-row flex-col`">
    <div :class="`${styles.flexStart} flex-1 flex-col xl:px-0 sm:px-16 px-6`">
      <div class="flex flex-row items-center py-[6px] px-4 bg-discount-gradient rounded-[8px] mb-2">
        <img :src="discount" alt="discount" class="w-[32px] h-[32px]">
        <p class="font-poppins font-bold text-[14px] text-white ml-2">Get 20% discount on your first order</p>
      </div>
      <div class="flex flex-row justify-between items-center w-full">
        <h1 class="flex-1 font-poppins font-semibold ss:text-[72px] text-[52px] text-white ss:leading-[100px] leading-[75px]">
          The Next <br class="sm:block hidden">
          <span class="text-gradient">Generation</span>
        </h1>
        <div class="ss:flex hidden md:mr-4 mr-0">
          <GetStarted/>
        </div>
      </div>
      <h1 class="font-poppins font-semibold ss:text-[68px] text-[52px] text-white ss:leading-[100px] leading-[75px] w-full">
        Payment Method.</h1>
      <p :class="`${styles.paragraph} max-w-[470px] mt-5`">
        Our team of experts uses a methodology to identify the credit cards most likely to fit your needs.
        We examine annual percentage rates, annual fees.
      </p>
    </div>
    <div :class="`${styles.flexCenter} flex-1 flex md:my-0 my-10 relative xl:left-[10rem]`">
      <img :src="robot" alt="robot" class="w-[100%] h-[100%] relative z-50 xl:left-[10rem]">
      <div class="absolute top-0  w-[40%] h-[35%] pink__gradient z-0"/>
      <div class="absolute bottom-0 rounded-full w-[80%] h-[80%] white__gradient z-10"/>
      <div class="absolute right-20 bottom-20 w-[50%] h-[50%] blue__gradient z-0"/>
    </div>
    <div :class="`${styles.paddingY} ss:hidden`">
      <GetStarted/>
    </div>
  </section>
</template>

<style scoped>
</style>
