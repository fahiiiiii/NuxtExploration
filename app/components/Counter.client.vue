<template>
  <BaseCard title="🖥️ Client-Side Counter">
    <div class="counter">
      <p>This component only runs on the client-side!</p>
      <div class="counter-display">
        <span class="count">{{ count }}</span>
      </div>
      <div class="counter-controls">
        <BaseButton @click="decrement" variant="danger">-</BaseButton>
        <BaseButton @click="increment" variant="success">+</BaseButton>
        <BaseButton @click="reset" variant="secondary">Reset</BaseButton>
      </div>
      <p><small>Current time: {{ currentTime }}</small></p>
    </div>
  </BaseCard>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const count = ref(0)
const currentTime = ref('')

const increment = () => count.value++
const decrement = () => count.value--
const reset = () => count.value = 0

onMounted(() => {
  // This will only run on the client
  const updateTime = () => {
    currentTime.value = new Date().toLocaleTimeString()
  }
  updateTime()
  setInterval(updateTime, 1000)
})
</script>

<style scoped>
.counter {
  text-align: center;
}

.counter-display {
  margin: 20px 0;
}

.count {
  font-size: 3rem;
  font-weight: bold;
  color: #007bff;
  display: inline-block;
  min-width: 100px;
}

.counter-controls {
  margin: 20px 0;
}
</style>