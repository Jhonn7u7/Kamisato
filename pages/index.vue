<template>
  <NuxtLayout>
    <template #hero>
      <header class="min-h-screen flex justify-start items-center relative overflow-hidden">
        <div class="flex-1 flex flex-col items-center justify-center text-center max-w-3xl mx-auto lg:mx-0 space-y-10">
          <span class="uppercase text-5xl md:text-8xl font-black text-indigo-700">
            <h2>Join the Kamisato community</h2>
          </span>
          <ul class="flex justify-center items-center w-full gap-5">
            <li class="animation-text p-2 hover:shadow-lg hover:bg-violet-200 rounded-xl text-indigo-700">
              <svg-discord class="block w-14 h-14" />
            </li>
            <li class="animation-text p-2 hover:shadow-lg hover:bg-violet-200 rounded-xl text-indigo-700">
              <svg-facebook class="block w-14 h-14" />
            </li>
          </ul>
        </div>
        <img src="/images/hero-2.webp" class="absolute blur-sm md:blur-none -z-10 bottom-0 right-0 h-full object-cover"
          width="600" alt="">
      </header>
    </template>
    <section id="main" class="my-5">
      <header class="text-center space-y-4 text-indigo-800">
        <h2 class="text-4xl font-bold">Noticias</h2>
        <div class="flex justify-between items-center max-w-7xl mx-auto px-6">
          <span class="inline-block text-xl font-extralight">Lo mas recientes sobre el videojuego</span>
          <a href="#" class="flex justify-center items-center gap-1 font-medium">
            <span>Ver todo</span>
            <svg-arrow-left class="stroke-indigo-800" />
          </a>
        </div>
      </header>
      <div
        class="mt-10 mx-auto max-w-7xl px-4 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 place-content-center place-items-center">
        <!-- Card -->
        <div v-for="(article, i) in articles" :key="i"
          class="animation-text max-w-sm p-4 bg-indigo-500 rounded-xl shadow-2xl hover:bg-indigo-600">
          <div class="flex justify-between items-center text-xl font-medium capitalize">
            <span class="text-white">{{  article.title  }}</span>
            <span
              class="inline-flex justify-center items-center text-gray-200 text-xs py-1 px-2 bg-indigo-500 rounded-full">{{
               article.createdAt  }}</span>
          </div>
          <div class="space-y-2 leading-relaxed">
            <p class="text-base font-light text-gray-300">{{  article.description  }}</p>
            <nuxt-link :to="article._path"
              class="inline-flex justify-center items-center gap-1 capitalize text-gray-100"> Leer mas
              <svg-arrow-left class="block stroke-white" />
            </nuxt-link>
          </div>
        </div>
      </div>
    </section>
    <section id="characters" class="mb-5 z-0">
      <header class="text-center space-y-4 text-indigo-800">
        <h2 class="text-4xl font-bold">Personajes</h2>
        <div class="flex justify-between items-center max-w-7xl mx-auto px-6">
          <span class="inline-block text-xl font-extralight">Conocé a todos y a cada uno</span>
          <a href="#" class="flex justify-center items-center gap-1 font-medium">
            <span>Ver todos</span>
            <svg-arrow-left class="stroke-indigo-800" />
          </a>
        </div>
      </header>
      <div
        class="mt-32 mx-auto max-w-7xl px-4 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-28 place-content-center place-items-center z-0">
        <nuxt-link v-for="(heroe, i) in heroes" :key="i" :to="heroe._path"
          class="animation-text bg-indigo-500 hover:bg-indigo-600 hover:scale-105 text-indigo-800 hover:text-white shadow-2xl p-4 rounded-xl relative min-h-fit w-full z-0">
          <figure class="-mt-28 z-0 flex justify-center">
            <img :src="heroe.images[0]" class="mx-auto" width="200" height="auto" :alt="heroe.name">
          </figure>
          <div class="flex flex-row justify-between items-end">
            <div class="flex-1 leading-snug">
              <span
                class="inline-flex justify-center items-center py-0 px-3 font-medium bg-indigo-800 text-white rounded-full">{{
                 heroe.calification  }}</span>
              <span class="block uppercase font-semibold text-xl">{{  heroe.clasification  }}</span>
              <span class="block text-4xl font-black">{{  heroe.name  }}</span>
            </div>
            <div class="flex-none">
              <img :src="getElement(heroe.element)" width="100" height="100" alt="Mona">
            </div>
          </div>
        </nuxt-link>
      </div>
    </section>
  </NuxtLayout>
</template>

<script setup lang="ts">
const loadArticles = async () => {
  try {
    const articles = await queryContent('/news').without('body').find()
    return articles
  } catch (error) {
    throw createError({ statusCode: 500, message: 'Error to load articles' })
  }
}
const loadHeroes = async () => {
  try {
    const heroes = await queryContent('/characters').without('body').find()
    return heroes
  } catch (error) {
    throw createError({ statusCode: 500, message: 'Error to load articles' })
  }
}
const [articles, heroes] = await Promise.all([loadArticles(), loadHeroes()])

const elements = {
  'FIRE': '/images/demo.png'
}

const getElement = (element: string) => {
  const elementUppercased = element.toUpperCase()
  return elements[elementUppercased]
}

</script>
