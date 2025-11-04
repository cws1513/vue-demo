<template>
  <div>{{ fullName }}</div>
</template>

<script setup>
import { ref, computed, onMounted } from 'vue'

const firstName = ref('woosung')
const lastName = ref('choi')

const fullName = computed(() => {
  return firstName.value + " " + lastName.value
})

onMounted(() => {
  console.log('mounted');

  let a = 10;
  setTimeout(() => {
    console.log('setTimeout');
    a = 20;
    console.log(a);
  }, 500);

  setTimeout(() => {
    lastName.value = "123"
  }, 1000);

  setTimeout(() => {
    firstName.value = "CWS"
  }, 1000);
})
</script>