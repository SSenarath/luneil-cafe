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
                    <NuxtLink id="nav-product" to="/products">
                        Products
                    </NuxtLink>
                </el-menu-item>
                <el-menu-item index="2">
                    <NuxtLink to="/cart">
                        Cart
                    </NuxtLink>
                </el-menu-item>
            </div>
            
            
        </el-menu>
        
        <div class="p-10 xl:p-20 text-xxs sm:text-xl md:text-2xl xl:text-4xl pb-16">
            <div class="flex gap-x-2 mb-5 m:mb-10">
                <NuxtLink  class="product-selection m:p-2 bg-gray-200 border-black border-2" to="/products">
                    All
                </NuxtLink>
                <NuxtLink class="product-selection m:p-2 bg-gray-200 border-black border-2" to="/products/shorteatsandsnacks">
                    Short Eats & Snacks
                </NuxtLink>
                <NuxtLink class="product-selection m:p-2 bg-gray-200 border-black border-2" to="/products/hoppersandcurries">
                    Hoppers and Curries
                </NuxtLink>
                
            </div>
            <slot />
        </div>
        <div class="bg-white mt-auto" >
            <p class="text-xs text-center py-2 border-t">© 2023 Sanduni Senarath & Hiruni Senarath</p>
        </div>
    </div>
</template>

<script setup>
    
</script>

<style scoped>
    .router-link-exact-active {
    background-color: #fde68a;
  }

  #nav-product {
    background-color: white;
  }
    
</style>