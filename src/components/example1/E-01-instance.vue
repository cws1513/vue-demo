<template>
  <div>Hello, {{ message }}</div>
</template>

<script setup>
import { ref } from 'vue'

const name = 'woosung';
const message = ref(name);
</script>

<style scoped>
div {
  color: blue;
  font-size: 20px;
  font-weight: bold;
}
</style>