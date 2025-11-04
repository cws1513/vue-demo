<template>
  <div>
    <ChildComponent
        :message="parentMessage"
        :id = "1"
        :password = "1234"
        @custom-event="handleEvent"
    />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import ChildComponent from './ChildComponent.vue'

const parentMessage = ref('Hello from parent')

function handleEvent(payload) {
  console.log(payload)
}
</script>