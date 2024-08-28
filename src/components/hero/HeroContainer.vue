<template>
  <section class="vh-100 d-flex justify-content-center align-items-center">
    <div class="container py-5">
      <div class="row flex-lg-row-reverse align-items-center g-md-5 py-5 responsive-spacing">
        <slot name="picture"></slot>
        <slot></slot>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "HeroContainer",
  props: ["delay"],
};
</script>

<style>
@media (max-width: 768px) {
  .responsive-spacing {
    gap: 3rem;
  }
}
</style>
