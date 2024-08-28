<template>
  <div class="col-lg-5 center-content">
    <h1 class="display-5 fw-bold lh-1 mb-4">
      <slot name="introduce"></slot>
    </h1>
    <p class="lead mb-4 text">
      <slot></slot>
    </p>
  </div>
</template>

<script>
export default {
  props: ["delay"],
};
</script>

<style>
.center-content {
  margin: 0 auto;
}

.text{
  padding-top:10px
}

@media (max-width: 768px) {
  .center-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
}
</style>
