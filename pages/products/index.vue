<template>
    <div class="flex flex-wrap justify-between">
        <ProductCard v-for="p in shorteats" :product="p"/>
        <ProductCard v-for="p in hoppersandcurries" :product="p"/>
    </div>
   
</template>

<script setup>
    definePageMeta({
        layout:'products'
    })
    const {data: shorteats} = await useFetch('http://localhost:5003/shorteatsandsnacks/')
    const {data: hoppersandcurries} = await useFetch('http://localhost:5003/hoppersandcurries/')
    

</script>

<style scoped>
    .router-link-exact-active {
    color: #12b488;
  }

</style>