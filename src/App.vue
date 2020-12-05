<template>
  <div id="app">
    <footer class="page-footer bg-success text-white pt-2">
    <component-footer></component-footer>
  </footer>
  </div>
  

</template>

<script>
import componentFooter from './components/componentFooter.vue';
export default {
  components: { componentFooter },
  name: "App",
};
</script>

