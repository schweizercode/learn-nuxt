<template>
    <div>
        <p>Prouct Detilas for {{id}}</p>
        <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias nisi non et quod obcaecati deleniti. Non neque magnam numquam temporibus delectus quae soluta aliquid rem, dolore, quia dolor aspernatur consequuntur?</p>
    </div>
</template>

<script setup>
const { id } = useRoute().params

definePageMeta({
    layout: "products"
})
</script>

  
<style scoped>

</style>