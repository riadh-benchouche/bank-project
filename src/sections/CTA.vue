<script setup lang="ts">
// @ts-ignore
import styles from "../styles.js";
// @ts-ignore
import ButtonComponent from "../components/ButtonComponent.vue";
</script>

<template>
  <section :class="`${styles.flexCenter} ${styles.marginY} ${styles.padding} sm:flex-row flex-col bg-black-gradient-2 rounded-[20px] box-shadow`">
    <div class="flex-1 flex flex-col">
      <h2 :class="styles.heading2">Let’s try our service now!</h2>
      <p :class="`${styles.paragraph} max-w-[470px] mt-5`">
        Everything you need to accept card payments and grow your business
        anywhere on the planet.
      </p>
    </div>

    <div :class="`${styles.flexCenter} sm:ml-10 ml-0 sm:mt-0 mt-10`">
      <ButtonComponent msg="Get Started"/>
    </div>
  </section>
</template>
