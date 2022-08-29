<template>
  <NuxtLayout>
    <header class="min-h-[92vh] flex justify-start items-center relative overflow-hidden">
      <div class="flex-1 flex flex-col items-center justify-center text-center max-w-3xl mx-auto lg:mx-0 space-y-10">
        <span class="uppercase text-5xl md:text-8xl font-black text-indigo-700">
          <h2>Join the community</h2>
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
      <img src="/images/hero-2.webp" class="absolute blur-sm md:blur-none -z-10 bottom-0 right-0 h-full object-cover" width="600" alt="">
    </header>
    <br>
    <h2 class="text-center text-indigo-700 text-lg font-bold ">Noticias</h2>
    <p class="text-indigo-600 text-center text-lg">Lo mas recientes sobre el videojuego.<span ><a href="" class="inline-flex font-bold"> Ver mas noticias<svg-arrow-left-more-info class="block stroke-2"/></a></span></p>
    <section class="grid grid-cols-4 space-x-1.5 m-2  "> <!--contenedor de tarjetas noticias-->
       <div class="p-6 bg-indigo-500 rounded-xl shadow-2xl max-ws-sm  hover:bg-indigo-600">  <!--card init -->
      <div class="flex justify-between items-center text-xl font-medium capitalize">
        <span class="text-white">reinicio del servidor</span>
        <span class="text-gray-200 text-sm">reciente</span>
      </div>
      <div class="space-y-2 leading-relaxed">
        <p class="text-base font-light text-gray-300">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nihil reprehenderit soluta tempore officiis</p>
        <a href="#" class="inline-flex justify-center items-center gap-1 capitalize text-gray-100"> Leer mas<svg-arrow-left class="block stroke-2"/></a>
      </div>
       </div> <!--card final -->
    </section > <!-- fin del contenedor de tarjetas noticias-->
  </NuxtLayout>
</template>
