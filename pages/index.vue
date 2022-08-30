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
        <span class="inline-block text-xl font-extralight">Lo mas recientes sobre el videojuego</span>
      </header>
      <div
        class="mt-10 mx-auto max-w-7xl px-4 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 place-content-center place-items-center">
        <a href="#" class="block animation-text max-w-sm p-6 bg-indigo-500 rounded-xl shadow-2xl hover:bg-indigo-600"
          v-for="i in 7">
          <div class="flex justify-between items-center text-xl font-medium capitalize">
            <span class="text-white">reinicio del servidor</span>
            <span class="text-gray-200 text-sm">reciente</span>
          </div>
          <div class="space-y-2 leading-relaxed">
            <p class="text-base font-light text-gray-300">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nihil
              reprehenderit soluta tempore officiis</p>
            <a href="#" class="inline-flex justify-center items-center gap-1 capitalize text-gray-100"> Leer mas
              <svg-arrow-left class="block stroke-2" />
            </a>
          </div>
        </a>
      </div>
    </section>
  </NuxtLayout>
</template>
