<template>
  <div class="home">
    <BaseCard title="🎉 Welcome to Nuxt 3 Component Demo">
      <div class="intro">
        <p>This project demonstrates various Nuxt 3 component features:</p>
        
        <div class="features-grid">
          <div class="feature">
            <h4>📦 Auto-Import</h4>
            <p>Components are automatically imported from the <code>components/</code> directory</p>
          </div>
          
          <div class="feature">
            <h4>🏗️ Nested Structure</h4>
            <p>Components in subdirectories like <code>base/Button.vue</code> become <code>&lt;BaseButton&gt;</code></p>
          </div>
          
          <div class="feature">
            <h4>🖥️ Client Components</h4>
            <p>Components with <code>.client.vue</code> extension only run on the client</p>
          </div>
          
          <div class="feature">
            <h4>🏭 Server Components</h4>
            <p>Components with <code>.server.vue</code> extension are pre-rendered on the server</p>
          </div>
          
          <div class="feature">
            <h4>⚡ Lazy Loading</h4>
            <p>Use <code>Lazy</code> prefix to load components only when needed</p>
          </div>
          
          <div class="feature">
            <h4>🔄 Dynamic Components</h4>
            <p>Switch between components dynamically using <code>&lt;component :is="..."&gt;</code></p>
          </div>
        </div>
        
        <div class="cta">
          <NuxtLink to="/components-demo">
            <BaseButton variant="primary">🚀 See Components in Action</BaseButton>
          </NuxtLink>
        </div>
      </div>
    </BaseCard>
  </div>
</template>

<style scoped>
.intro {
  text-align: center;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin: 30px 0;
}

.feature {
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 8px;
  border-left: 4px solid #007bff;
}

.feature h4 {
  margin: 0 0 10px 0;
  color: #333;
}

.feature code {
  background-color: #e9ecef;
  padding: 2px 6px;
  border-radius: 3px;
  font-size: 0.9em;
}

.cta {
  margin-top: 40px;
}
</style>