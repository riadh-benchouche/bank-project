<script setup lang="ts">
// @ts-ignore
import styles from "../styles.js";
// @ts-ignore
import {logo} from "../assets/index.js";
// @ts-ignore
import {footerLinks, socialMedia} from "../DB/index.js";
</script>

<template>
  <section :class="`${styles.flexCenter} ${styles.paddingY} flex-col`">
    <div :class="`${styles.flexStart} md:flex-row flex-col mb-8 w-full`">
      <div class="flex-[1] flex flex-col justify-start mr-10">
        <img
            :src=logo
            alt="hoobank"
            class="w-[266px] h-[72.14px] object-contain"
        />
        <p :class="`${styles.paragraph} mt-4 max-w-[312px]`">
          A new way to make the payments easy, reliable and secure.
        </p>
      </div>

      <div class="flex-[1.5] w-full flex flex-row justify-between flex-wrap md:mt-0 mt-10">
        <div v-for="footerlink in footerLinks" :key="footerlink.title" class="flex flex-col ss:my-0 my-4 min-w-[150px]">
          <h4 class="font-poppins font-medium text-[18px] leading-[27px] text-white">
            {{ footerlink.title }}
          </h4>
          <ul class="list-none mt-4">
            <li
                v-for="link in footerlink.links"
                :key=link.name
                :class="`font-poppins font-normal text-[16px] leading-[24px] text-dimWhite hover:text-secondary
                cursor-pointer ${ link.name !== '' ? 'mb-4' : 'mb-0' }`"> {{ link.name }}
            </li>
          </ul>
        </div>
        ))}
      </div>
    </div>

    <div
        class="w-full flex justify-between items-center md:flex-row flex-col pt-6 border-t-[1px] border-t-[#3F3E45]">
      <p class="font-poppins font-normal text-center text-[18px] leading-[27px] text-white">
        Copyright Ⓒ 2022 HooBank. All Rights Reserved.
      </p>

      <div class="flex flex-row md:mt-0 mt-6">
        <a v-for="social in socialMedia" :href="social.link" target="_blank">
          <img

              :key=social.id
              :src=social.icon
              :alt=social.id
              :class="`w-[21px] h-[21px] object-contain cursor-pointer ${ social.id !== 'social-media-4' ? 'mr-6' : 'mr-0'} `"
          />
        </a>
      </div>
    </div>
  </section>
</template>
