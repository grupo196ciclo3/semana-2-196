<template>
  <div id="app">

    <componente-nav></componente-nav>

    <!-- v-for="(item,index) of team" :key="index" -->

    <!-- <team-card v-bind:member="item"></team-card> -->

  </div>
</template>

<script>

// import TeamCard from "./components/TeamCard.vue"
import ComponenteNav from "./components/ComponenteNav.vue"
// import ComponenteApi from "./components/ComponenteApi.vue"

export default {
  name: 'App',
  components:{
    // TeamCard,
    ComponenteNav
    // ComponenteApi,
  },
  team: []
}
</script>

