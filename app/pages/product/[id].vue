<template>
    <div>
        <h2>This page carries Product Details</h2>
        <h2>{{id}}</h2>

        <NuxtLink to="/index">Home</NuxtLink>
        <NuxtLink to="/about">About</NuxtLink>
        <NuxtLink to="/portfolio">Portfolio</NuxtLink>
    </div>
</template>

<script setup>
    const id = useRoute().params.id;
</script>

<style lang="scss" scoped>

</style>