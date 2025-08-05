<template>
  <header class="header">
    <div class="header-content">
      <h1>🚀 Nuxt 3 Component Demo</h1>
      <nav>
        <NuxtLink to="/" class="nav-link">Home</NuxtLink>
        <NuxtLink to="/components-demo" class="nav-link">Components Demo</NuxtLink>
      </nav>
    </div>
  </header>
</template>

<style scoped>
.header {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 1rem 0;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}
.header-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-link {
  color: white;
  text-decoration: none;
  margin-left: 20px;
  padding: 8px 16px;
  border-radius: 4px;
  transition: background-color 0.3s;
}

.nav-link:hover {
  background-color: rgba(255,255,255,0.2);
}
</style>