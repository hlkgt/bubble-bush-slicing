<script setup>
import { ref } from "vue";
const clients = ref([
  {
    title: "Website My Hospital",
    description:
      "Very nice to work with Bubble Bash, a reliable and responsive team is very helpful",
    photoProfile: "src/assets/profil-1.png",
    username: "khatty clock",
    position: "CEO My Hospital",
  },
  {
    title: "Logo F&B Corp",
    description:
      "Really the best service we've ever gotten, really looking forward to the next project",
    photoProfile: "src/assets/profil-2.png",
    username: "john robert",
    position: "CEO My Hospital",
  },
  {
    title: "Supermarket Mobile Apps",
    description:
      "The best developer team ever, it's a lot of fun working. Maybe work together again on the next project?",
    photoProfile: "src/assets/profil-3.png",
    username: "khatty clock",
    position: "CEO My Hospital",
  },
]);
</script>

<template>
  <div class="container-fluid px-5">
    <div class="row">
      <div class="col-md-12 my-5 px-5">
        <span class="text-capitalize">client reviews</span>
        <h1 class="text-capitalize">what our happy client say about us</h1>
      </div>
      <div class="col-md-6 col-xl-4 px-5 mb-5" v-for="client in clients">
        <div class="card-client d-flex flex-column gap-2 py-4 px-3">
          <h1 class="title">{{ client.title }}</h1>
          <p>{{ client.description }}</p>
          <div class="d-flex align-items-center gap-2">
            <img :src="client.photoProfile" :alt="client.title" />
            <div class="d-flex flex-column align-items-center">
              <h1 class="username">{{ client.username }}</h1>
              <p>{{ client.position }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.card-client {
  border: 4px solid #000000;
}
.title {
  font-size: 1.5rem;
}
.username {
  font-size: 1.2rem;
}
</style>
