<script setup>
import { ref } from "vue";

const links = ref([
  {
    linkTo: "Home",
  },
  {
    linkTo: "Our Service",
  },
  {
    linkTo: "Portofolio",
  },
  {
    linkTo: "Testimonial",
  },
  {
    linkTo: "Contact Us",
  },
]);

const explores = ref([
  {
    name: "Resources",
  },
  {
    name: "Blog",
  },
  {
    name: "Documents",
  },
]);
const companys = ref([
  {
    name: "About Us",
  },
  {
    name: "Partners",
  },
  {
    name: "Customers",
  },
  {
    name: "Contact Us",
  },
]);

const icons = ref(["facebook", "twitter", "instagram", "linkedin"]);
</script>

<template>
  <div class="container-fluid my-5 px-5">
    <div class="row px-5 gap-4">
      <div class="col-md-6 mb-4">
        <div class="d-flex align-items-center gap-2 mb-3">
          <img src="../assets/logo.png" alt="logo" />
          <h1 class="text-capitalize fs-3">bubble bash</h1>
        </div>
        <p>
          Introducing, We are Bubble Bash digital agency company with <br />
          more than 6 years of experience. We are committed to serve <br />
          with all our heart
        </p>
        <div class="d-flex gap-4">
          <font-awesome-icon
            :icon="['fab', icon]"
            size="2x"
            v-for="icon in icons"
          />
        </div>
      </div>
      <div class="col-md-6 row">
        <div class="col-6 col-md-4 mb-4">
          <h1 class="fs-4">Pages</h1>
          <ul class="list-unstyled">
            <li class="mb-2" v-for="link in links">
              {{ link.linkTo }}
            </li>
          </ul>
        </div>
        <div class="col-6 col-md-4">
          <h1 class="fs-4">Explore</h1>
          <ul class="list-unstyled">
            <li class="mb-2" v-for="explore in explores">
              {{ explore.name }}
            </li>
          </ul>
        </div>
        <div class="col-sm-6 col-md-4">
          <h1 class="fs-4">Company</h1>
          <ul class="list-unstyled">
            <li class="mb-2" v-for="company in companys">
              {{ company.name }}
            </li>
          </ul>
        </div>
      </div>
      <div class="col-12 text-center d-flex justify-content-end">
        <h1 class="fs-6">
          &copy; References,
          <a
            target="_blank"
            href="https://codedesign.dev/challenge/bubble-bash"
            class="text-black text-decoration-none"
            >"codedesign - bubble bash"
          </a>
        </h1>
      </div>
    </div>
  </div>
</template>
