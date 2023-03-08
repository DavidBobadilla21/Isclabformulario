<script>
import axios from "axios";
let API_URL = `/api/guardarPersonasUxd.php`;
export default {
  data() {
    return {
      nombre: "",
      edad: "",
      estadoCivil: "",
      trabajo: "",
      residencia: "",
      cita: "",
      citaAutor: "",
      bio: "",
      personalidad01: "",
      personalidad02: "",
      personalidad03: "",
      personalidad04: "",
      objetivos: "",
      frustraciones: "",
      motivaciones: "",
      porcentaje: "",
      marcas: "",
    };
  },
  methods: {
    summit() {
      API_URL + this.pagina;
      console.log(API_URL);
      axios.post("/api/guardarPersonasUxd.php", {
        nombre: this.nombre,
        edad: this.edad,
        estadoCivil: this.estadoCivil,
        trabajo: this.trabajo,
        residencia: this.residencia,
        cita: this.cita,
        citaAutor: this.citaAutor,
        bio: this.bio,
        personalidad01: this.personalidad01,
        personalidad02: this.personalidad02,
        personalidad03: this.personalidad03,
        personalidad04: this.personalidad04,
        objetivos: this.objetivos,
        frustraciones: this.frustraciones,
        motivaciones: this.motivaciones,
        porcentaje: this.porcentaje,
        marcas: this.marcas,
        //completar las variables, estas deben llamarse como las que se recibirán en el backend sin el símbolo del dolar $
      })
        .then((response) => {
          console.log(response.status)
        });
    },
  },
};

</script>
<template>
  <div class="grid grid-cols-3">
    <div></div>
    <div>
      <form class="w-full max-w-lg">









        <div class="flex flex-wrap -mx-3 mb-6">
          <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="residencia">
              RESIDENCIA
            </label>
            <input v-model="residencia"
              class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
              id="residencia" type="string" placeholder="  ">
          </div>

          <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="cita">
              CITA
            </label>
            <input v-model="cita"
              class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
              id="cita" type="text" placeholder="  ">
          </div>

        </div>
        <div class="flex flex-wrap -mx-3 mb-6">
          <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="citaAutor">
              CITA AUTOR
            </label>
            <input v-model="citaAutor"
              class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
              id="citaAutor" type="text" placeholder="  ">
          </div>

          <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="bio">
              BIO
            </label>
            <input v-model="bio"
              class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
              id="bio" type="string" placeholder="22">
          </div>
        </div>

        <div class="flex flex-wrap -mx-3 mb-6">
          <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="personalidad01">
              PERSONALIDAD 1
            </label>
            <input v-model="personalidad01"
              class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
              id="personalidad01" type="text" placeholder="  ">
          </div>

          <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="personalidad02">
              PERSONALIDAD 2
            </label>
            <input v-model="personalidad02"
              class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
              id="personalidad02" type="string" placeholder="22">
          </div>
        </div>

        <div class="flex flex-wrap -mx-3 mb-6">
          <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="personalidad03">
              PERSONALIDAD 3
            </label>
            <input v-model="personalidad03"
              class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
              id="personalidad03" type="text" placeholder="  ">
          </div>

          <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="personalidad04">
              PERSONALIDAD 4
            </label>
            <input v-model="personalidad04"
              class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
              id="personalidad04" type="string" placeholder="22">
          </div>
        </div>

        <div class="flex flex-wrap -mx-3 mb-6">
          <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="objetivos">
              OBJETIVOS
            </label>
            <input v-model="objetivos"
              class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
              id="objetivos" type="text" placeholder="  ">
          </div>

          <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="frustraciones">
              FRUSTRACIONES
            </label>
            <input v-model="frustraciones"
              class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
              id="frustraciones" type="string" placeholder="22">
          </div>
        </div>

        <div class="flex flex-wrap -mx-3 mb-6">
          <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="motivaciones">
              MOTIVACIONES
            </label>
            <input v-model="motivaciones"
              class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
              id="motivaciones" type="text" placeholder="  ">
          </div>

          <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="porcentaje">
              PORCENTAJES
            </label>
            <input v-model="porcentaje"
              class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
              id="porcentaje" type="string" placeholder="22">
          </div>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="marcas">
            MARCAS
          </label>
          <input v-model="marcas"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="marcas" type="string" placeholder="22">
        </div>

        <button @click="summit()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
          ENVIAR

        </button>

      </form>
    </div>
    <div> </div>
  </div>

  <section class="bg-gray-100">
    <div class="grid grid-cols-3">
      <div></div>
    <div class="mx-auto max-w-screen-xl px-4 py-16 sm:px-6 lg:px-8">
      <div>


        <div class="rounded-lg bg-white p-8 shadow-lg lg:col-span-3 lg:p-12">
          <form action="" class="space-y-4">
            <div>
              <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="nombre">
                Nombre
              </label>
              <input v-model="nombre" class="w-full rounded-lg border-gray-200 p-3 text-sm" id="nombre" type="text"
                placeholder="David Bobadilla Verde">

            </div>

            <div class="grid grid-cols-1 gap-4 sm:grid-cols-2">
              <div>
                <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="edad">
                  Edad
                </label>
                <input v-model="edad" class="w-full rounded-lg border-gray-200 p-3 text-sm" id="edad" type="string"
                  placeholder="22">
              </div>

              <div>
                <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="estadoCivil">
                  ESTADO CIVIL
                </label>
                <div class="relative">
                  <select v-model="estadoCivil" class="w-full rounded-lg border-gray-200 p-3 text-sm" id="estadoCivil">
                    <option>Soltero 1</option>
                    <option>Casado 2</option>
                    <option>Divorciado 3</option>
                    <option>Separado 4</option>
                    <option>Unión libre 5</option>
                    <option>Viudo 6</option>
                  </select>
                </div>
              </div>
            </div>

            <div class="grid grid-cols-1 gap-4 sm:grid-cols-2">
              <div>
                <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="trabajo">
              TRABAJO
            </label>
            <input v-model="trabajo"
            class="w-full rounded-lg border-gray-200 p-3 text-sm"
              id="trabajo" type="text" placeholder=" ">
              </div>

              <div>
                <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="residencia">
              Residencia
            </label>
            <input v-model="residencia"
            class="w-full rounded-lg border-gray-200 p-3 text-sm"
              id="residencia" type="string" placeholder="  ">
            </div>
          </div>
            <div>
              <label class="sr-only" for="message">Message</label>

              <textarea class="w-full rounded-lg border-gray-200 p-3 text-sm" placeholder="Message" rows="8"
                id="message"></textarea>
            </div>

            <div class="mt-4">
              <button type="submit"
                class="inline-block w-full rounded-lg bg-black px-5 py-3 font-medium text-white sm:w-auto">
                Send Enquiry
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
    <div></div>
  </div>
  </section>
</template>