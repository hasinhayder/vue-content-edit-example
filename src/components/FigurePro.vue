<script setup>
import { ref } from 'vue'
const props = defineProps({
    image: String,
    title: String,
    edit: Boolean
})

const imageSrc = ref(props.image)

const images = [
    'https://images.unsplash.com/photo-1601134991665-a020399422e3?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mjd8fG1vYmlsZSUyMHBob3RvZ3JhcGh5fGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
    'https://images.unsplash.com/photo-1545081576-5b7e640c083a?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mzh8fG1vYmlsZSUyMHBob3RvZ3JhcGh5fGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
    'https://images.unsplash.com/photo-1547416400-e55d9817e9cd?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NDd8fG1vYmlsZSUyMHBob3RvZ3JhcGh5fGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
    'https://images.unsplash.com/photo-1614443890409-2bc89f8ba3ad?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NjR8fG1vYmlsZSUyMHBob3RvZ3JhcGh5fGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
    'https://images.unsplash.com/photo-1562433745-a78af0fc7487?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NzB8fG1vYmlsZSUyMHBob3RvZ3JhcGh5fGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60'
]

const showChoice = ref(false)

function displayModal() {
    if (props.edit == true) {
        showChoice.value = true
    }

}

function selectImage(index) {
    imageSrc.value = images[index]
    showChoice.value = false
}

</script>
<template>
    <slot>
        <figure class="flex items-center flex-col" v-if="!showChoice">
            <img @click="displayModal()" class="w-full" :src="imageSrc" alt="" :class="{'cursor-pointer':edit}">
            <figcaption class="text-sm text-gray-500 mx-auto">
                {{ title }}
            </figcaption>
        </figure>
        <div class="p-10 border border-gray-400" v-if="showChoice">
            <div class="flex space-x-2">
                <div v-for="(image, index) in images">
                    <img :key="index" @click="selectImage(index)" :src="image" class="w-[100px] cursor-pointer" />
                </div>
            </div>
            <button @click="showChoice = false" class="mt-10 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">Close</button>
        </div>
    </slot>
</template>
<style scoped></style>