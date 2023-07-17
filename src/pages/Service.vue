<script setup>
import { ref } from "vue";
const services = ref([
  {
    imageUrl: "src/assets/figma-logo.png",
    title: "UI/UX Designer",
    description:
      "We are ready to make your website more friendly and efficient in the eyes of users",
  },
  {
    imageUrl: "src/assets/code.png",
    title: "Web Development",
    description:
      "Want to create a website that has many features? We have the answer for you. ",
  },
  {
    imageUrl: "src/assets/article-medium.png",
    title: "Content Writer",
    description:
      "We provide interesting content and can attract customers for you",
  },
  {
    imageUrl: "src/assets/presentation-chart.png",
    title: "Branding",
    description:
      "Create visual branding with amazing result, you just sit back and relax",
  },
  {
    imageUrl: "src/assets/video-camera.png",
    title: "Editing Video",
    description:
      "Want to create a website that has many features? We have the answer for you. ",
  },
  {
    imageUrl: "src/assets/pen-nib.png",
    title: "Illustration",
    description:
      "Create beauty illustrasion as you need, and make it interesting",
  },
]);
</script>

<template>
  <div class="container-fluid px-5">
    <div class="row">
      <div class="col-md-12 my-5 px-5">
        <span class="text-capitalize">our service</span>
        <h1 class="text-capitalize">we provide what you need</h1>
      </div>
      <div class="col-md-6 col-xl-4 px-5 mb-5" v-for="service in services">
        <div
          class="card shadow-lg d-flex align-items-center gap-3 flex-column py-4 px-3 text-center"
        >
          <img
            :src="service.imageUrl"
            :alt="service.title"
            class="img-fluid"
            width="60"
          />
          <h1>{{ service.title }}</h1>
          <p>{{ service.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container-fluid {
  margin-top: 50rem;
  background-color: #f9f9f9;
}
.card h1 {
  font-size: 1.5rem;
}

@media (max-width: 1199.98px) {
  .container-fluid {
    margin-top: 30rem;
  }
}
@media (max-width: 575.98px) {
  .container-fluid {
    margin-top: 15rem;
  }
}
</style>
