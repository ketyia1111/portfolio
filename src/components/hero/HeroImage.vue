<template>
  <div class="col-10 col-sm-7 col-lg-7">
    <img
      class="d-block mx-lg-auto img-fluid"
      loading="lazy"
      :src="require(`@/assets/${src}`)"
    />
  </div>
</template>

<script>
export default {
  props: ["src"],
};
</script>

<style>
.col-10 {
  margin: 0 auto;
}
@media (max-width: 768px) {
  .col-10 {
    display: flex;
    justify-content: center;
  }
}
</style>
