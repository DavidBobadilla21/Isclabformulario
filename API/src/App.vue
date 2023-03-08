<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
    <header class=" bg-blue-700">
      <div class="wrapper">

        <nav class=" bg-blue-700">
          <div class="grid grid-cols-3">
            <div></div>
            <div class=" bg-blue-700">
              <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />
            </div>
            <div></div>
          </div>
        </nav>
      </div>
      <div class="grid grid-cols-5 items-center text-xxl text-white">
        <div></div>
        <div class=""> <button
            class=" bh-14 sm:h-10 px-7 font-semibold rounded-md bg-green-800 mb-8 justify-center shadow-xl hover:shadow-inner transition duration-500 ease-in-out  transform hover:-translate-x hover:scale-105">
            <RouterLink to="/">Home</RouterLink>
          </button></div>
        <div class="..."><button
            class="h-14 sm:h-10 px-7 font-semibold rounded-md bg-green-800  mb-8 justify-center shadow-xl hover:shadow-inner transition duration-500 ease-in-out  transform hover:-translate-x hover:scale-105">
            <RouterLink to="/about">About</RouterLink>
          </button></div>
        <div class="..."><button
            class="h-14 sm:h-10 px-7 font-semibold rounded-md bg-green-800  mb-8 justify-center shadow-xl hover:shadow-inner transition duration-500 ease-in-out  transform hover:-translate-x hover:scale-105">
            <RouterLink to="/about" class="py-5">Ver ingresados</RouterLink>
          </button></div>
        <div></div>
      </div>
    </header>





  <RouterView />
</template>
