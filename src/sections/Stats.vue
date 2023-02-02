<script setup lang="ts">
// @ts-ignore
import {stats} from "../DB/index.js";
// @ts-ignore
import styles from "../styles.js";
</script>

<template>
  <section :class="`${styles.flexCenter} flex-row flex-wrap sm:mb-20 mb-6`">
    <div v-for="stat in stats" :class="`flex-1 flex justify-start items-center flex-row m-3`">
      <h4 class="font-poppins font-semibold xs:text-[40px] text-[30px] xs:leading-[53px] leading-[43px] text-white">
        {{ stat.value }}</h4>
      <p class="font-poppins font-normal xs:text-[20px] text-[15 px] xs:leading-[26px] leading-[21px] text-gradient uppercase ml-3">
        {{ stat.title }}</p>
    </div>
  </section>
</template>

<style scoped>
</style>
