<script setup lang="ts">
import {reactive} from 'vue'
// @ts-ignore
import {close, logo, menu} from "../assets/index.js";
// @ts-ignore
import {navLinks} from "../DB/index.js";

const state = reactive({
  toggle: false,
  active: '' as string,
})
</script>

<template>
  <nav class="w-full flex py-6 justify-between items-center navbar">
    <img :src="logo" alt="hoobank" class="w-[124px] h-[32px]">
    <ul class="list-none sm:flex hidden justify-end items-center flex-1">
      <li v-for="nav in navLinks" class="font-poppins font-normal cursor-pointer text-[16px] text-white">
        <a :href="`#${nav.id}`"
           :class="`${state.active === nav.title ? 'text-white' : 'text-dimWhite' } ${nav.id === navLinks[3].id ? 'mr-0' : 'mr-10'}` "
           @click="state.active = nav.title">{{ nav.title }}</a>
      </li>
    </ul>
    <div class="sm:hidden flex flex-1 justify-end items-center">
      <img :src="state.toggle ? close : menu" @click="state.toggle = !state.toggle" alt="menu"
           class="w-[28px] h-[28px] object-contain">
      <div :class="state.toggle ? 'flex' : 'hidden'"
           class="p-6 bg-black-gradient absolute top-20 right-0 mx-4 my-2 min-w-[140px] rounded-xl ">
        <ul class="list-none justify-end items-start flex-col">
          <li v-for="nav in navLinks" class="font-poppins font-normal cursor-pointer text-[16px] text-white"
          >
            <a :href="`#${nav.id}`"
               :class="`${state.active === nav.title ? 'text-white' : 'text-dimWhite' } ${ nav.id === navLinks[3].id ? 'mb-0' : 'mb-4'}`"
               @click="state.active = nav.title">{{ nav.title  }}</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
</style>
