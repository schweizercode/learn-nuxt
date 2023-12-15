<template>
    <div>
<div class="grid grid-cols-4 gap-5">
    <div v-for="product in products" :key="product.id">
        <nuxt-link :to="`/products/${product.id}`">
            <div class="bg-white shadow-sm rounded-md p-4">
                <img :src="product.image" :alt="product.title" class="w-full h-48 object-cover rounded-md">
                <h3 class="font-bold text-lg">{{product.title}}</h3>
                <p class="text-gray-500">{{product.price}}</p>
            </div>
        </nuxt-link>
    </div>
</div>
    </div>
</template>

<script setup>
definePageMeta({
    layout: "products"
})

//fetch products
const { data: products } = await useFetch("https://fakestoreapi.com/products")
</script>

<style  scoped></style>