<template>
  <div id="app">
    <UiHeader />
    <main class="container">
      <NuxtPage />
    </main>
    <UiFooter />
  </div>
</template>

<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f5f5f5;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
  min-height: 80vh;
}
</style>