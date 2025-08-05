<template>
  <div class="demo-page">
    <BaseCard title="🧪 Interactive Component Playground">
      <p>Explore different Nuxt 3 component features below:</p>
    </BaseCard>

    <!-- Server Component -->
    <ServerTime />

    <!-- Client Component -->
    <Counter />

    <!-- Dynamic Component Demo -->
    <SomeComponent />

    <!-- Lazy Loaded Component -->
    <div class="lazy-section">
      <h2>Scroll down to see lazy loading in action!</h2>
      <div style="height: 100px;"></div>
      <LazyImageGallery />
    </div>

    <!-- Component Composition Demo -->
    <BaseCard title="🔧 Component Composition Example">
      <p>This shows how components can be composed together:</p>
      
      <div class="button-showcase">
        <BaseButton variant="primary">Primary Button</BaseButton>
        <BaseButton variant="secondary">Secondary Button</BaseButton>
        <BaseButton variant="success">Success Button</BaseButton>
        <BaseButton variant="danger">Danger Button</BaseButton>
        <BaseButton :loading="true">Loading Button</BaseButton>
        <BaseButton disabled>Disabled Button</BaseButton>
      </div>

      <template #footer>
        <p><small>All these buttons use the same <code>&lt;BaseButton&gt;</code> component with different props!</small></p>
      </template>
    </BaseCard>
  </div>
</template>

<style scoped>
.demo-page {
  margin-bottom: 40px;
}

.lazy-section {
  text-align: center;
  margin: 60px 0;
}

.button-showcase {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
  margin: 20px 0;
}

code {
  background-color: #e9ecef;
  padding: 2px 6px;
  border-radius: 3px;
  font-size: 0.9em;
}
</style>