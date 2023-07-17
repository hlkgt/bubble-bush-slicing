<script setup>
const text = defineProps(["text"]);
</script>

<template>
  <button>{{ text.text }}</button>
</template>

<style scoped>
button {
  padding: 23px 32px;
  color: #2a2c3d;
  font-size: 20px;
  font-weight: bold;
}

@media (max-width: 575.98px) {
  button {
    padding: 13px 22px;
    color: #2a2c3d;
    font-size: 20px;
    font-weight: bold;
  }
}
</style>
