<template>
    <div class="flex flex-wrap justify-between">
        <div v-if="type === 'shorteatsandsnacks'">
            
            <ProductCard v-for="p in shorteats" :product="p"/>
        </div>
        <div v-if="type === 'hoppersandcurries'">
            <ProductCard  v-for="p in hoppersandcurries" :product="p"/>
        </div>
    </div>
</template>

<script setup>
     const { type } = useRoute().params
     definePageMeta({
        layout:'products'
    })
    const {data: shorteats} = await useFetch('http://localhost:5003/shorteatsandsnacks/')
    const {data: hoppersandcurries} = await useFetch('http://localhost:5003/hoppersandcurries/')



</script>

<style scoped>

</style>