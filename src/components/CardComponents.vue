<script setup lang="ts">
// @ts-ignore
import styles, {layout} from "../styles.js";
// @ts-ignore
import {card} from '../assets/index.js';
// @ts-ignore
import ButtonComponent from "./ButtonComponent.vue";
</script>

<template>
  <section :class="layout.section">
    <div :class="layout.sectionInfo">
      <h2 :class="styles.heading2">
        Find a better card deal <br class="sm:block hidden"/> in few easy
        steps.
      </h2>
      <p :class="`${styles.paragraph} max-w-[470px] mt-5`">
        Arcu tortor, purus in mattis at sed integer faucibus. Aliquet quis
        aliquet eget mauris tortor.ç Aliquet ultrices ac, ametau.
      </p>
      <ButtonComponent styles="mt-10" msg="Get Started"/>
    </div>

    <div :class="layout.sectionImg">
      <img :src=card alt="billing" class="w-[100%] h-[100%]"/>
    </div>
  </section>
</template>
