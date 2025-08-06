<template>
    <div>
        <h2>This page carries Product Details</h2>
        <h2>ID: {{id}}</h2>

        <ProductList />
        <ProductDetails />
        
    </div>
</template>

<script setup>
    const id = useRoute().params.id;
     useHead({
        title:"Product page"
    })
</script>

<style lang="scss" scoped>

</style>