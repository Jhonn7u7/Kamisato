<template>
    <nuxt-layout>
        <div class="flex flex-col md:flex-row">
            <header class="px-4 mt-5 max-w-7xl mx-auto">
                <span class="space-y-2 text-indigo-900">
                    <h1 class="text-3xl md:text-4xl font-extrabold">{{  heroe.name  }}</h1>
                    <span class="flex justify-between items-center gap-1 text-xl font-medium">
                        <span>{{  heroe.clasification  }}</span>
                        <div class="inline-flex justify-center items-center gap-1">
                            <svg-star v-for="i in heroe.calification"
                                class="block w-5 h-5 stroke-indigo-900 fill-yellow-300" />
                        </div>
                    </span>
                </span>
                <div class="flex md:flex-col-reverse justify-between items-center md:gap-4">
                    <div class="flex-none">
                        <div class="flex flex-col md:flex-row flex-nowrap gap-4">
                            <figure v-for="(image, i) in heroe.images" :key="i" @click="selectedImage = i || 0"
                                class="block p-2 rounded-2xl bg-violet-300 animation-text active:scale-105">
                                <img :src="image" class="w-14 h-14 md:w-24 md:h-24 object-contain" width="50"
                                    height="50" :alt="i + ''">
                            </figure>
                        </div>
                    </div>
                    <div class="flex-1">
                        <img :src="heroe.images[selectedImage]" class="object-contain" width="300" height="500"
                            :alt="heroe.name">
                    </div>
                </div>
            </header>
            <section class="overview mt-5 px-4 max-w-7xl mx-auto">
                <content-renderer tag="article" class="prose prose-base prose-indigo" :value="heroe"></content-renderer>
            </section>
        </div>
    </nuxt-layout>
</template>

<script setup lang="ts">
const route = useRoute()

const loadHeroe = async () => {
    try {
        const heroe = await queryContent(`/characters/${route.params.character}`).findOne()
        return heroe
    } catch (error) {
        throw createError({ statusCode: 404, statusMessage: 'Page Not Found' })
    }
}
const heroe = await loadHeroe()
const selectedImage = ref<number>(0)

</script>