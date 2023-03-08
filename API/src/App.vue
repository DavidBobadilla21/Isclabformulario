<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>



<template>
  <nav class="flex items-center bg-gray-800 p-3 flex-wrap">
    <a href="#" class="p-2 mr-4 inline-flex items-center">
      <img alt="Vue logo" class="logo fill-current text-white h-8 w-8 mr-2" src="@/assets/LOGOSCARRERAS-02.png" />
      <span class="text-xl text-white font-bold uppercase tracking-wide">ISCLAB</span>
    </a>
    <button
      class="text-white inline-flex p-3 hover:bg-gray-900 rounded lg:hidden ml-auto hover:text-white outline-none nav-toggler"
      data-target="#navigation">
      <i class="material-icons">
        MENÚ
      </i>
    </button>
    <div class="hidden top-navbar w-full lg:inline-flex lg:flex-grow lg:w-auto" id="navigation">
      <div
        class="lg:inline-flex lg:flex-row lg:ml-auto lg:w-auto w-full lg:items-center items-start  flex flex-col lg:h-auto">
        <a href="#"
          class="lg:inline-flex lg:w-auto w-full px-3 py-2 rounded text-gray-400 items-center justify-center hover:bg-gray-900 hover:text-white">
          <span>
            <RouterLink to="/">Home</RouterLink>
          </span>
        </a>
        <a href="#"
          class="lg:inline-flex lg:w-auto w-full px-3 py-2 rounded text-gray-400 items-center justify-center hover:bg-gray-900 hover:text-white">
          <span>
            <RouterLink to="/about">Registrar</RouterLink>
          </span>
        </a>
        <a href="#"
          class="lg:inline-flex lg:w-auto w-full px-3 py-2 rounded text-gray-400 items-center justify-center hover:bg-gray-900 hover:text-white">
          <span>
            <RouterLink to="/personas" class="py-5">Ver ingresados</RouterLink>
          </span>
        </a>

      </div>
    </div>
  </nav>
  <RouterView />

  <footer class="bg-black" aria-labelledby="footer-heading">
  <h2 id="footer-heading" class="sr-only">Footer</h2>

  <div class="px-4 py-10 mx-auto bg-black max-w-7xl sm:px-6 lg:px-16">
    <div class="flex flex-wrap items-baseline lg:justify-center">
      <span class="mt-2 text-sm font-light text-gray-500">
        Copyright © 2020 - 2021
        <a href="https://wickedlabs.dev" class="mx-2 text-wickedblue hover:text-white" rel="noopener noreferrer">@wickedlabsHQ</a>. Since 2020
      </span>
    </div>
  </div>
</footer>

</template>
