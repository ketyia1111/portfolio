<template>
  <section class="p-3 p-lg-5">
    <div class="container">
      <div class="row">
        <h2 class="my-md-5 mb-3 text-center">経験してることやりたいこと</h2>
        <div v-for="(skill, index) in skills" :key="index" class="col-sm-12 col-md-4 mb-3">
          <div class="text-center">
            <img
              v-if="skill.image"
              class="mb-3"
              :src="require(`@/assets/${skill.image}`)"
              data-aos="fade-up"
              :data-aos-delay="delay"
              data-aos-anchor-placement="top-bottom"
            />
            <h4
              class="mb-3"
              data-aos="fade-up"
              :data-aos-delay="delay + 100"
              data-aos-anchor-placement="top-bottom"
            >
              {{ skill.title }}
            </h4>
            <div>
              {{ skill.description }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import skills from "@/data/skills";

export default {
  data() {
    return {
      skills,
      delay: 0, // 適切な値を設定してください
    };
  },
};
</script>

<style scoped>
h2 {
  color: #2c3e50;
}
h4 {
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
