<script setup lang="ts">
// @ts-ignore
import styles from './styles.js'
import NavBar from "./sections/NavBar.vue";
import Hero from "./sections/Hero.vue";
import Stats from "./sections/Stats.vue";
import Business from "./sections/Business.vue";
import Billing from "./sections/Billing.vue";
import CardComponents from "./components/CardComponents.vue";
import Testimonials from "./sections/Testimonials.vue";
import Clients from "./sections/Clients.vue";
import CTA from "./sections/CTA.vue";
import FooterBar from "./sections/FooterBar.vue";
</script>

<template>
  <div class="bg-primary w-full overflow-hidden">
    <div :class="`${styles.paddingX} ${styles.flexStart}`">
      <div :class="`${styles.boxWidth}`">
        <NavBar/>
      </div>
    </div>
    <div :class="`bg-primary ${styles.flexStart}`">
      <div :class="`${styles.boxWidth}`">
        <Hero/>
      </div>
    </div>
    <div :class="`bg-primary ${styles.paddingX} ${styles.flexStart}`">
      <div :class="`${styles.boxWidth}`">
        <Stats/>
        <Business/>
        <Billing/>
        <CardComponents/>
        <Testimonials/>
        <Clients/>
        <CTA/>
        <FooterBar/>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>
