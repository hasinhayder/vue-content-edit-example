<script setup>
import {ref} from 'vue'
const props = defineProps({
    image: String,
    title: String
})    
</script>
<template>
    <figure class="flex items-center flex-col">
        <img class="w-full" :src="image" alt="">
        <figcaption class="text-sm text-gray-500 mx-auto">
            {{  title }}
        </figcaption>
    </figure>
</template>
<style scoped></style>