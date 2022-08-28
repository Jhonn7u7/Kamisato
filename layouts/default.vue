<script setup lang="ts">
const isNavbarActive = ref(false)
</script>

<template>
  <div class="px-2 md:px-0">
    <nav
      class="sticky top-0 min-h-[8vh] flex justify-between items-center text-indigo-700 font-bold text-base uppercase select-none px-4 bg-violet-200 z-20">
      <h2 class="font-['Concert_One'] text-xl md:text-3xl font-extrabold">
        <span>Agencia Kamisato</span>
      </h2>
      <ul class="md:inline-flex gap-4 hidden">
        <li class="nav-button animation-text hover:text-white">
          <a href="#">Incio</a>
        </li>
        <li class="nav-button animation-text hover:text-white">
          <a href="#">Personajes</a>
        </li>
        <li class="nav-button animation-text hover:text-white">
          <a href="#">Noticias</a>
        </li>
        <li class="nav-button animation-text hover:text-white">
          <a href="#">Comunidad</a>
        </li>
      </ul>
      <a href="#"
        class="hidden animation-text md:inline-flex justify-center items-center h-10 px-4 bg-indigo-700 text-white hover:text-indigo-700 hover:bg-white rounded-full hover:shadow-2xl hover:shadow-purple-400 gap-1">
        <span>Ingresa</span>
        <svg-door class="inline-block w-4 h-4" />
      </a>

      <button @click="isNavbarActive = !isNavbarActive"
        class="animation-text bg-trasparent md:hidden active:scale-110 active:bg-white inline-flex justify-center items-center p-2 rounded-full">
        <svg-menu class="block w-7 h-7" />
      </button>

      <div
        class="animation-text block md:hidden min-h-screen fixed top-0 right-0 bg-indigo-700 translate-x-0 w-10/12 rounded-l-lg p-4 text-violet-200"
        :class="[isNavbarActive ? 'translate-x-0' : 'translate-x-full']">
        
      </div>

    </nav>
    <slot></slot>
  </div>
</template>

<style>
* {
  -webkit-tap-highlight-color: transparent;
}

.animation-text {
  @apply transition-all ease-linear duration-150;
}

.nav-button {
  @apply flex justify-center items-center h-10 px-4;
}
</style>