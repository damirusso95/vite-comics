<!-- qui va js -->
<script>
// IMPORTO IL COMPONENTE HEADER
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppJumbo from './components/AppJumbo.vue';





export default {
  // CREO UNA 'LISTA' DI COMPONENTI
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    AppJumbo,

  },
  data() {
    return {

    }
  },
  methods: {

  },
  mounted() {

  }
}
</script>

<!-- qui va html -->
<template>
  <!-- RICHIAMO L'HEADER -->
  <AppHeader />
  <!-- RICHIAMO IL MAIN -->
  <AppMain />
  <AppJumbo/>
  <!-- RICHIAMO IL FOOTER -->
  <AppFooter />
</template>
<!-- qui va css -->
<style></style>
