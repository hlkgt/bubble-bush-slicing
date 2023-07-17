<script setup>
import { ref } from "vue";
const services = ref([
  {
    imageUrl: "src/assets/portofolio-1.png",
    title: "Website My Hospital",
    description:
      "Create a hospital website with patient, doctor, and drug logistics features that help hospital operations",
  },
  {
    imageUrl: "src/assets/portofolio-2.png",
    title: "Food & Beverages Corp Logo",
    description:
      "Create a logo for a food & beverage company, with emphasis on aesthetics and user requests",
  },
  {
    imageUrl: "src/assets/portofolio-3.png",
    title: "Supermarket Mobile Apps",
    description:
      "Develop mobile applications for supermarkets with buy, auto-pay, and marketplace features",
  },
]);
</script>

<template>
  <div class="container-fluid px-5">
    <div class="row">
      <div class="col-md-12 my-5 px-5">
        <span class="text-capitalize">our portofolio's</span>
        <h1 class="text-capitalize">recent projects</h1>
      </div>
      <div class="col-md-6 col-xl-4 px-5 mb-5" v-for="service in services">
        <div class="d-flex flex-column gap-2 py-4 px-3">
          <img
            :src="service.imageUrl"
            :alt="service.title"
            class="img-fluid mx-auto"
          />
          <h1>{{ service.title }}</h1>
          <p>{{ service.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
h1 {
  font-size: 1.5rem;
}

@media (max-width: 1199.98px) {
}
@media (max-width: 575.98px) {
}
</style>
