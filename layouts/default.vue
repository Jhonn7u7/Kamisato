<template>
  <div>
    <nav class="min-h-[8vh] flex justify-between items-center text-indigo-700 font-bold text-base uppercase">
      <h2 class="font-['Concert_One'] text-3xl font-extrabold">
        <span>Agencia Kamisato</span>
      </h2>
      <ul class="inline-flex gap-4">
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
        class="animation-text inline-flex justify-center items-center h-10 px-4 bg-violet-800 text-white hover:text-violet-800 hover:bg-white rounded-full hover:shadow-2xl hover:shadow-purple-400 gap-1">
        <span>Ingresa</span>
        <svg-door class="inline-block w-4 h-4" />
      </a>
    </nav>
    <slot></slot>
  </div>
</template>

<style>
.animation-text {
  @apply transition-all ease-linear duration-150;
}

.nav-button {
  @apply flex justify-center items-center h-10 px-4;
}
</style>