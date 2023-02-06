<template>
    <div class="flex flex-wrap justify-between">
        <ProductCard v-if="type === 'shorteatsandsnacks'" v-for="p in shorteats" :product="p"/>
        <ProductCard  v-if="type === 'hoppersandcurries'" v-for="p in hoppersandcurries" :product="p"/>
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