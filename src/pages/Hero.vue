<script setup>
import { ref } from "vue";

const informations = ref([
  {
    infTitle: "12K+",
    infDesc: "Happy Client",
  },
  {
    infTitle: "6K+",
    infDesc: "Worldwide Clients",
  },
  {
    infTitle: "6+",
    infDesc: "Years of Experience",
  },
  {
    infTitle: "12+",
    infDesc: "Award Winners",
  },
]);
const links = ref([
  {
    name: "home",
    path: "/",
  },
  {
    name: "our service",
    path: "/",
  },
  {
    name: "portofolio",
    path: "/",
  },
  {
    name: "testimonial",
    path: "/",
  },
  {
    name: "contact us",
    path: "/",
  },
]);
</script>

<template>
  <nav class="navbar navbar-expand-lg px-5 position-fixed z-3 w-100">
    <div class="container-fluid">
      <a
        class="navbar-brand text-capitalize text-white d-flex align-items-center"
        href="#"
      >
        <img src="../assets/logo.png" alt="logo" />
        bubble bash
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="text-white">Menu</span>
      </button>
      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav gap-4">
          <li class="nav-item" v-for="link in links">
            <a class="nav-link text-white text-capitalize" href="#">{{
              link.name
            }}</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
  <div
    class="hero container-fluid text-white px-5 text-center d-flex justify-content-center align-items-center flex-column position-relative"
  >
    <h1 class="title">
      Creating Amazing Digital Product <br />
      For Your Business
    </h1>
    <p class="description">
      We are a professional digital agency that has been established since 2016,
      we present a variety of digital services that can help you solve problems
      in your business
    </p>
    <button>Get Started -></button>
    <div class="position-absolute px-5">
      <img src="../assets/hehe.png" alt="hehe" />
      <div class="row text-black">
        <div
          class="col-3 d-flex justify-content-center align-items-centerr flex-column"
          v-for="information in informations"
        >
          <h1 class="information">{{ information.infTitle }}</h1>
          <p class="information-description">{{ information.infDesc }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.navbar {
  background-color: #2f6b4f;
}
.navbar-brand {
  font-size: 1.6rem;
  font-weight: 600;
}
.nav-link {
  font-size: 1.4rem;
}
.hero {
  background-color: #2f6b4f;
  min-height: 100vh;
}
.title {
  font-size: 4rem;
  margin-bottom: 3rem;
}
.description {
  width: 50%;
  margin-bottom: 3rem;
  color: rgba(255, 255, 255, 0.7);
}
button {
  padding: 23px 32px;
  color: #2a2c3d;
  font-size: 20px;
  font-weight: bold;
}
.position-absolute {
  bottom: -42rem;
}
.position-absolute img {
  width: 100%;
  padding-bottom: 50px;
}
.information {
  font-size: 32px;
}
.information-description {
  font-size: 18px;
}

@media (max-width: 575.98px) {
  .title {
    margin-bottom: 1rem;
    font-size: 2rem;
  }
  .description {
    width: 100%;
    margin-bottom: 1rem;
    font-size: 0.8rem;
  }
  button {
    padding: 13px 22px;
    color: #2a2c3d;
    font-size: 20px;
    font-weight: bold;
  }
  .position-absolute {
    bottom: -10rem !important;
  }
  .position-absolute img {
    width: 100%;
    padding-bottom: 30px;
  }
  .information {
    font-size: 20px;
  }
  .information-description {
    font-size: 8px;
  }
}
@media (max-width: 1199.98px) {
  .position-absolute {
    bottom: -25rem;
  }
}
</style>
