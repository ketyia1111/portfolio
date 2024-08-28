<template>
  <div>
    <h2 class="my-md-5 mb-3 text-center">資格</h2>
    <div v-for="license in licenses" :key="license.id" class="license-container">
      <h3>{{ license.position }}</h3>
      <ul>
        <li v-for="desc in license.description" :key="desc.id">
          {{ desc.description }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import licenses from "@/data/licenses";

export default {
  data() {
    return {
      licenses,
    };
  },
};
</script>

<style scoped>
h2 {
  color: #2c3e50;
}
h3 {
  padding: 10px 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  background: #ecf0f1;
  margin: 5px 0;
  padding: 10px;
  border-radius: 4px;
}
.license-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 10px;
  border-radius: 10px;
  background: #f8f9fa;
}
@media (max-width: 800px) {
  .license-container {
    max-width: 100%;
    padding: 5px;
  }
}
</style>
