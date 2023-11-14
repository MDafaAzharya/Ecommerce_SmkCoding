<script lang="ts" setup>
import { useProductsStore } from "~/stores/products";

const productStore = useProductsStore();
const { products } = storeToRefs(productStore);
productStore.getAllProducts();

const selectedCategory = ref("");
</script>

<template>
  <section>
    <div class="container">
      <div class="py-10">
        <div class="mb-6 flex justify-end gap-6">
          <NuxtLink to="/category/create" class="bg-slate-600 text-white flex justify-center items-center px-3 rounded-lg">Create Category</NuxtLink>
          <NuxtLink to="/product/create" class="bg-slate-600 text-white flex justify-center items-center px-3 rounded-lg">Create Products</NuxtLink>
          <Dropdown @selected-category="selectedCategory = $event" />
        </div>
        <div class="flex gap-6 flex-wrap mx-auto">
          <template v-for="(product, index) in products" :key="index" >
            <CardsCardProduct :product="product" class="w-[calc(100%/4-18px)]" />
          </template>
        </div>
      </div>
    </div>
  </section>
</template>
