<template>
  <AppHeader :links="links">keita portfolio</AppHeader>
  <HeroSection id="hero" pic="header.png">
    <template v-slot:introduce>Hey WhatUp!!</template>
    こんにちは～<b>けいた</b>です！！<br />
    セキュリティとプログラミング学習中～<br />
    職業はEC系のC#エンジニアです。<br />
    インフラ、セキュリティにも携われるかも♪
  </HeroSection>
  <SkillsGrid id="skills"/>
  <LicenseTable id="edu-exp" :licenses="licenses" />
  <AppFooter :copyright="copyright" />
</template>

<script>
import AppHeader from './components/common/Header.vue';
import AppFooter from './components/common/Footer.vue';
import HeroSection from "@/components/hero/HeroSection.vue";
import SkillsGrid from "@/components/skills/SkillGrid.vue";
import LicenseTable from "@/components/license/LicenseTable.vue";

export default {
  name: 'App',
  data: () => {
    return {
      delay: 100,
      links: [
        {
          name: "home",
          url: "#hero",
        },
        {
          name: "skills",
          url: "#skills",
        },
        {
          name: "license",
          url: "#edu-exp",
        },
      ],
      copyright: "2024 Keita Yokoyama",
    };
  },
  components: {
    AppHeader,
    AppFooter,
    HeroSection,
    SkillsGrid,
    LicenseTable
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
