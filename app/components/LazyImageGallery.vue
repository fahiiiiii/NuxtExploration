<template>
  <BaseCard title="🖼️ Lazy Loaded Image Gallery">
    <div class="gallery">
      <p>This component demonstrates lazy loading. Scroll down to see it load!</p>
      <div class="image-grid">
        <div 
          v-for="i in 6" 
          :key="i" 
          class="image-placeholder"
        >
          <div class="placeholder-content">
            <span>🎨</span>
            <p>Image {{ i }}</p>
          </div>
        </div>
      </div>
    </div>
  </BaseCard>
</template>

<style scoped>
.gallery {
  text-align: center;
}

.image-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 15px;
  margin-top: 20px;
}

.image-placeholder {
  height: 120px;
  background: linear-gradient(45deg, #f0f0f0, #e0e0e0);
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  animation: pulse 2s infinite;
}

.placeholder-content {
  text-align: center;
}

.placeholder-content span {
  font-size: 2rem;
  display: block;
  margin-bottom: 5px;
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.7; }
}
</style>