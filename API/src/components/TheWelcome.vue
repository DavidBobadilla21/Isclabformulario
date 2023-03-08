
<template>
  <section class="relative bg-[url(https://fondosmil.com/fondo/58596.jpg)] bg-cover bg-center bg-no-repeat">
    <div class="absolute inset-0 bg-white/75 sm:bg-transparent sm:bg-gradient-to-r sm:from-white/95 sm:to-white/25"></div>

    <div class="relative mx-auto max-w-screen-xl px-4 py-32 sm:px-6 lg:flex lg:h-screen lg:items-center lg:px-8">
      <div class="max-w-xl text-center sm:text-left">
        <h1 class="text-3xl font-extrabold sm:text-5xl">
          ¿Que es una persona ?

          <strong class="block font-extrabold text-blue-700">
            ISCLAB.
          </strong>
        </h1>

        <p class="mt-4 max-w-lg sm:text-xl sm:leading-relaxed">
          Persona se refiere a uno o unos personajes ficticios creados con motivo de representar a los usuarios posibles
          de un producto a través de una buena cantidad de investigaciones cualitativas y cuantitativas. Persona nos
          contesta la pregunta “¿Para quién diseñamos?” Es una herramienta poderosa basada en conclusiones de
          investigaciones en ayudar la creación de funciones de producto optimizando la investigación de UX. No sólo
          representa a algún usuario concreto sino al conjunto de ellos, se puede entender como el personaje típico de la
          conducta, la actitud, las habilidades y los contextos de todos los usuarios potenciales.
        </p>

        <div class="mt-8 flex flex-wrap gap-4 text-center">
          <a href="#"
            class="block w-full rounded bg-blue-600 px-12 py-3 text-sm font-medium text-white shadow hover:bg-blue-700 focus:outline-none focus:ring active:bg-blue-500 sm:w-auto">
            <RouterLink to="/about">Registraté!</RouterLink>
          </a>

          <a href="#"
            class="block w-full rounded bg-white px-12 py-3 text-sm font-medium text-blue-600 shadow hover:text-blue-700 focus:outline-none focus:ring active:text-blue-500 sm:w-auto">
            <RouterLink to="//personas">Ver ingresados</RouterLink>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
