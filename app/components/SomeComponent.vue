<template>
  <BaseCard title="🎯 Dynamic Component Demo">
    <div class="dynamic-demo">
      <p>This demonstrates dynamic component loading:</p>
      
      <div class="component-selector">
        <BaseButton 
          v-for="comp in availableComponents" 
          :key="comp.name"
          @click="currentComponent = comp.component"
          :variant="currentComponent === comp.component ? 'primary' : 'secondary'"
        >
          {{ comp.name }}
        </BaseButton>
      </div>
      
      <div class="dynamic-component-area">
        <component :is="currentComponent" />
      </div>
    </div>
  </BaseCard>
</template>

<script setup>
import { ref, resolveComponent } from 'vue'

const currentComponent = ref('ServerTime')

const availableComponents = [
  { name: 'Server Time', component: 'ServerTime' },
  { name: 'Counter', component: 'Counter' },
  { name: 'Image Gallery', component: 'LazyImageGallery' }
]
</script>

<style scoped>
.dynamic-demo {
  text-align: center;
}

.component-selector {
  margin: 20px 0;
}

.dynamic-component-area {
  margin-top: 30px;
  padding: 20px;
  background-color: #f8f9fa;
  border-radius: 8px;
  border: 2px dashed #dee2e6;
}
</style>