<template>
  <div id="app">
    <header>
      <ComponenteBanner></ComponenteBanner>
    </header>
    <main>
      <section id="services">
        <div class="container-fluid">
          <div class="row justify-content-center mb-5">
            <div
              class="col-sm-6 col-xs-12 col-lg-4 mt-5"
              v-for="(item, index) of servicios"
              :key="index"
            >
              <componente-servicios v-bind:partes="item"></componente-servicios>
            </div>
          </div>
        </div>
      </section>
      <section id="news">
        <componente-api></componente-api>
      </section>
      <section id="team">
        <div class="container-fluid">
          <div class="row justify-content-center mb-5">
            <div
              class="col mt-5 w-50"
              v-for="(item, index) of team"
              :key="index"
            >
              <team-card v-bind:member="item"></team-card>
            </div>
          </div>
        </div>
      </section>
      <!-- v-for="(item,index) of team" :key="index" -->
    </main>
    <footer class="page-footer bg-success text-white pt-2">
      <component-footer></component-footer>
    </footer>
  </div>
</template>
<script>
import TeamCard from "./components/TeamCard.vue";
import ComponenteBanner from "./components/ComponenteBanner.vue";
import ComponenteApi from './components/ComponenteApi.vue';
import ComponenteServicios from "./components/ComponenteServicios.vue";
import componentFooter from './components/componentFooter.vue'

export default {
  name: "App",
  components: {
    TeamCard,
    ComponenteBanner, 
    ComponenteApi,
    ComponenteServicios,
    componentFooter },
  data(){
    return{
      team: [
    {
      codigo: 1,
      nombre: "Andrés C Torres",
      descripcion: "Estudiante de Ing. Sistemas Cooperativa",
      rol: "Desarrollador Backend",
      image: require("./assets/Andres.jpg"),
    },
    {
      codigo: 2,
      nombre: "Javier C. Laiton",
      descripcion: "Ing. industrial egresado de Fundacion Universitaria CAFAM",
      rol: "Desarrollador Backend",
      image: require("./assets/Javier.jpeg"),
    },
    {
      codigo: 3,
      nombre: "Mayra Erazo",
      descripcion: "Biologa egresada de Universidad del Valle",
      rol: "Desarrollador Desarrollador Frontend",
      image: require("./assets/Mayra.jpg")
    },
    {
      codigo: 4,
      nombre: "José Olarte",
      descripcion: "Economista egresado de la Universidad de Cartagena",
      rol: "Desarrollador Backend",
      image: require("./assets/Jose.jpeg"),
    },
    {
      codigo: 5,
      nombre: "Iván González",
      descripcion: "Ingeniero Electronico egresado de la Universidad del Norte",
      rol: "Desarrollador Frontend",
      image: require("./assets/Ivan.jpg"),
    },
    {
      codigo: 6,
      nombre: "Julian Manrique",
      descripcion: "Ingeniero Quimico egresado de la Universidad Nacional",
      rol: "Desarrollador Frontend",
      image: require("./assets/Julian.jpg"),
    },
  ],servicios:[
        {
          titulo: "TRANSLATOR DEEPL",
          descripcion: "Software experto en idiomas encargados de transmitir mensajes escritos de un idioma a otro.",
          image: require("./assets/LogoDeepL.png"),
          boton:"Translator>>",
          url:"https://www.deepl.com/translator"

        }, 
        {
          titulo: "ENGLISH COURSE",
          descripcion: "Aprender inglés te abre muchas puertas, entra al sitio y aprende cosas de este idioma mundial.",
          image: require("./assets/learn1.png"), 
          boton:"Go To Learn >>",
          url:"https://www.curso-ingles.com/"
        },
        {
          titulo: "PRACTICE",
          descripcion: "Ademas de aprenderlo debes ponerlo en practica, practica con IsCollective.",
          image: require("./assets/Practice.jpg"),
          boton:"Go To Practice >>",
          url:"https://es.islcollective.com/"

        }
      ]
    }
  }
}
</script>