<template>
  <hero-container>
    <template v-slot:picture><hero-image :src="pic" /></template>
    <hero-text delay="200">
      <template v-slot:introduce><slot name="introduce"></slot></template>
      <slot></slot>
    </hero-text>
  </hero-container>
</template>

<script>
import HeroContainer from "./HeroContainer.vue";
import HeroText from "./HeroText.vue";
import HeroImage from "./HeroImage.vue";

export default {
  name: "HeroSection",
  props: ["pic"],
  components: {
    HeroText,
    HeroImage,
    HeroContainer,
  },
};
</script>