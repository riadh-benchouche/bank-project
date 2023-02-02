<script setup lang="ts">
// @ts-ignore
import styles from "../styles.js";
// @ts-ignore
import {clients} from "../DB/index.js";
</script>

<template>
  <section :class="`${styles.flexCenter} my-2`">
    <div :class="`${styles.flexCenter} flex-wrap w-full`">
      <div v-for="client in clients" :key=client.id
           :class="`flex-1 ${styles.flexCenter} sm:min-w-[192px] min-w-[120px] m-5`">
        <img :src=client.logo alt="client_logo" class="sm:w-[192px] w-[100px] object-contain"/>
      </div>
    </div>
  </section>
</template>
