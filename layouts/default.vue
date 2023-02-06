<template>
    <div class="flex flex-col h-screen">
        <el-menu
        :default-active="activeIndex"
        class="el-menu-demo"
        mode="horizontal"
        :ellipsis="false"
        @select="handleSelect"
         >
            <el-menu-item index="0">
                <NuxtLink to="/">
                    <img class="object-cover h-14 min-w-min lg:h-24" src="../assets/images/logo.png" alt="luneil cafe logo">
                </NuxtLink>
            </el-menu-item>
            <div class="ml-auto flex items-center">
                <el-menu-item index="1">
                    <NuxtLink to="/">
                        Products
                    </NuxtLink>
                </el-menu-item>
                <el-menu-item index="2">
                    <NuxtLink to="/orderform" class="">
                        Order Form
                    </NuxtLink>
                </el-menu-item>
            </div>
            
            
        </el-menu>
        <div class="p-10 xl:p-20 text-s sm:text-xl md:text-2xl xl:text-4xl pb-16">
            <slot -/>
        </div>
        <div class="bg-white mt-auto" >
            <p class="text-xs text-center py-2 border-t">© 2023 Sanduni Senarath & Hiruni Senarath</p>
        </div>
    </div>
</template>

<script setup>

</script>

<style scoped>
    
</style>