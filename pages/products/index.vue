<template>
    <!-- <div class="flex gap-x-2 mb-5 m:mb-10">
        <div v-for="(category,index) in categories">
            <button v-if="index === 0" class="product-selection m:p-2 bg-amber-200 border-black border-2" to="/products">
                {{category}}
            </button>
            <button v-else class="product-selection m:p-2 bg-gray-200 border-black border-2" to="/products">
                {{category}}
            </button>
        </div>
    </div> -->
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