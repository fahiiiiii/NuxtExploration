<template>
  <div>
    <Head>
      <Title>Home page here</Title>
    </Head>

    <h2>Hello from home page</h2>
    <Home />

    <h2>{{ state.number }}</h2>

    <button @click="increment">Increment</button>
    <button @click="decrement" v-if="state.number > 1">Decrement</button>
    <button @click="decrement" v-else disabled>Decrement</button>
  </div>
</template>

<script setup lang="ts">
useHead({
  meta: [
    { name: 'description', content: 'My amazing site.' }
  ]
})

const state = useState('counter', () => ({
  number: 1
}))

const increment = () => {
  state.value.number++
}
const decrement = () => {
  state.value.number--
}
</script>

<style lang="scss" scoped></style>
