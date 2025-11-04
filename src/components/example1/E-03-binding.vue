<template>
  <div>
    <input v-model="id" />
    <input v-model="password" />
    <p>{{ message }}</p>
    <button @click="whoami">whoami</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const message = ref('Hello Vue')
const id = ref('')
const password = ref('')

function whoami() {
  message.value = id.value + '' + password.value
}
</script>