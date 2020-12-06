<template>
  <div id="app">
    <section id="services">
    <div class="container-fluid">
      <div class="row justify-content-center mb-5" >
        <div class="col-sm-6 col-xs-12 col-lg-4 mt-5" v-for="(item,index) of servicios" :key="index">
          <componente-servicios v-bind:partes="item"></componente-servicios>
        </div>
      </div>
    </div>
    </section>
  </div>
</template>
<script>
import ComponenteServicios from "./components/ComponenteServicios.vue";

export default {
  name: "App",
  components: {
    ComponenteServicios
  },
  data(){
    return{
      servicios:[
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
          image: require("./assets/learn.png"), 
          boton:"Go To Learn >>",
          url:"https://www.curso-ingles.com/"
        },
        {
          titulo: "PRACTICE",
          descripcion: "Ademas de aprenderlo debes ponerlo en practica, practica con IsCollective.",
          image: require("./assets/Practice2.jpg"),
          boton:"Go To Practice >>",
          url:"https://es.islcollective.com/"

        }
      ]
    }
  }
};
</script>

