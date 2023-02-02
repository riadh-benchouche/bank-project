<script setup lang="ts">
// @ts-ignore
import {features} from '../DB/index.js';
// @ts-ignore
import styles, {layout} from "../styles.js";
// @ts-ignore
import ButtonComponent from "../components/ButtonComponent.vue";
// @ts-ignore
import FeatureCard from "../components/FeatureCard.vue";
</script>

<template>
  <section id="1" :class="layout.section">
    <div :class="layout.sectionInfo">
      <h2 :class="styles.heading2">You do the business, <br class="sm:block hidden">
        we'll handle the money.
      </h2>
      <p :class="`${styles.paragraph} max-w-[470px] mt-5`">With the right credit card, you can improve your financial
        life by building credit, earning rewards and saving money. But with hundreds of credit cards on the market.
      </p>
      <ButtonComponent styles="mt-10" msg="Get Started"/>
    </div>
    <div :class="`${layout.sectionImg} flex-col`">
      <FeatureCard v-for="feature in features" :feature="feature" :index="feature.id"/>
    </div>
  </section>
</template>
