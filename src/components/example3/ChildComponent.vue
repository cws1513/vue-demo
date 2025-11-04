<template>
  <div>
    <p>{{ message }}</p>
    <p>{{ id }}</p>
    <p>{{ password }}</p>
    <button @click="$emit('custom-event', 'Hello from child')">Send Event</button>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'ChildComponent',
  props: ['message', 'id', 'password'],
  emits: ['custom-event'],
  setup() {
    return {}
  }
})
</script>