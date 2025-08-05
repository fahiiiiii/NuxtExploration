<template>
  <BaseCard title="🏗️ Server-Side Component">
    <div class="server-info">
      <p>This component is rendered on the server only!</p>
      <p><strong>Server rendered at:</strong> {{ serverTime }}</p>
      <p><strong>Environment:</strong> {{ environment }}</p>
      <p><small>This content is pre-rendered and won't change on the client.</small></p>
    </div>
  </BaseCard>
</template>

<script setup>
// This runs only on the server
const serverTime = new Date().toISOString()
const environment = process.env.NODE_ENV || 'development'
</script>

<style scoped>
.server-info {
  background-color: #e8f5e8;
  padding: 15px;
  border-radius: 6px;
  border-left: 4px solid #28a745;
}
</style>