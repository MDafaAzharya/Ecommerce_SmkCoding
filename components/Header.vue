<template>
    <header class="w-full border-b border-slate-200 py-6 bg-sky-500 shadow-lg">
        <div class="container">
            <div class="flex justify-between items-center">
        <div>
        <NuxtLink to="/" class="text-xl font-bold text-sky-50">E-Commerce</NuxtLink>
        </div>
        <nav class="flex items-center gap-6 font-medium text-sky-50 ">
            <NuxtLink to="/" class="text-base hover:text-sky-950">Home</NuxtLink>
            
            <NuxtLink to="/product" class="text-
            base hover:text-sky-950">Products</NuxtLink>
            
            <NuxtLink to="/cart" class="text-base hover:text-sky-950">Cart</NuxtLink>
        </nav>
        </div>
        </div>
    </header>
</template>