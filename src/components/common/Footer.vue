<template>
  <footer class="bg-dark text-white text-center">
    <div class="text-center p-3">© {{ copyright }}</div>
  </footer>
</template>
<script>
export default {
  props: ["copyright"],
  name: "AppFooter",
};
</script>
<style></style>