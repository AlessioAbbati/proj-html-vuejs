<script>
import AppFooter from './components/AppFooter.vue'
import AppHeader from "./components/AppHeader.vue"
import AppMain from './components/AppMain.vue'
import 'bootstrap/dist/js/bootstrap.min.js';

export default {
  components: { 
    AppHeader,
    AppMain,
    AppFooter,
  },
}


</script>

<template>
  <div>
    <app-header />
    <app-main />
    <app-footer />
  </div>
</template>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap";
@import "@fortawesome/fontawesome-free/css/all.css";
</style>
