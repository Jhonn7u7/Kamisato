<template>
    <nuxt-layout>
        <header class="px-4 mt-5 max-w-7xl mx-auto flex flex-col">
            <div class="w-full overflow-hidden rounded-xl">
                <img src="https://images.unsplash.com/photo-1614102073832-030967418971" class="w-full h-52 object-cover"
                    :alt="article.cover">
            </div>
            <div
                class="animation-text bg-indigo-900 p-4 -mt-24 md:-mt-16 hover:bg-indigo-800 w-11/12 max-w-5xl mx-auto h-min rounded-xl text-indigo-300 space-y-2">
                <div class="flex flex-col md:flex-row justify-start md:justify-between items-start md:items-center">
                    <h1 class="font-bold text-2xl md:text-4xl">{{  article.title  }}</h1>
                    <span class="text-sm font-semibold">{{  article.createdAt  }}</span>
                </div>
                <p class="text-base md:text-lg font-light">
                    {{  article.description  }}
                </p>
            </div>
        </header>
        <section id="post" class="my-5 w-11/12 max-w-5xl mx-auto">
            <content-renderer tag="article" :value="article"></content-renderer>
        </section>
    </nuxt-layout>
</template>

<script setup lang="ts">
const route = useRoute()

const loadArticle = async () => {
    try {
        const article = await queryContent(`/news/${route.params.post}`).findOne()
        return article
    } catch (error) {
        throw createError({ statusCode: 404, message: 'Not Found' })
    }
}

const article = await loadArticle()
</script>