<script setup>
import Button from "../components/Button.vue";
</script>

<template>
  <div class="container-fluid h-50 text-white">
    <div class="row">
      <div
        class="col-md-12 d-flex justify-content-center align-items-center flex-column my-5 text-center"
      >
        <h1>
          Want a project idea and <br />
          want to make it come true?
        </h1>
        <p class="opacity-75">
          Please contact us and we will discuss about your project, don't forget
          we are <br />
          always here for you
        </p>
        <Button text="Contact Us" />
      </div>
    </div>
  </div>
</template>

<style scoped>
.container-fluid {
  background-color: #2f6b4f;
}
</style>
