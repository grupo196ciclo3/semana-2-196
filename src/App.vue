<template>
  <div id="app">
    <header>
      <ComponenteBanner></ComponenteBanner>
    </header>
    <main>
      <section id="team">
        <div class="container-fluid">
          <div class="row justify-content-center mb-5">
            <div class="col mt-5 w-50" v-for="(item,index) of team" :key="index">
              <team-card v-bind:member="item"></team-card>
            </div>
          </div>
        </div>
      </section>
      <section>
        <componente-api></componente-api>
      </section>
      <!-- v-for="(item,index) of team" :key="index" -->      
    </main>
  </div>
</template>

<script>
import TeamCard from "./components/TeamCard.vue";
import ComponenteBanner from "./components/ComponenteBanner.vue";
import ComponenteApi from './components/ComponenteApi.vue';

export default {
  name: "App",
  components: {
    TeamCard,
    ComponenteBanner, 
    ComponenteApi },
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
  ],
    }
  }
};
</script>

