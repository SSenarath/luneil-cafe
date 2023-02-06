<template>
    <div class="m-auto p-2 flex flex-col items-center gap-5 bg-white rounded-lg mb-4 border max-w-sm">
        <img :src="product.img" alt="cutlet" class="object-cover">
        <div class="text-sm border">
            <p class=" capitalize text-center border bg-amber-200 font-bold">{{product.category}}</p>
            <el-table :data="tableData" stripe style="width: 100%" size="small">
                <el-table-column prop="type" label="Filling" width="160" />
                <el-table-column prop="price" label="Price (CAD)" width="100" />
              </el-table>
        </div>
    </div>
</template>

<script setup>

    const {product} = defineProps(['product'])
    const tableData = product.options

</script>

<style scoped>

</style>