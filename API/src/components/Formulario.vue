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
          <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="nombre">
              NOMBRE
            </label>
            <input v-model="nombre"
              class="appearance-none block w-full bg-gray-200 text-gray-700 border border-grey-200 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
              id="nombre" type="text" placeholder="Jane">
          </div>
        </div>

        <button @click="summit()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
          ENVIAR

        </button>

      </form>
    </div>
    <div> </div>
  </div>
</template>