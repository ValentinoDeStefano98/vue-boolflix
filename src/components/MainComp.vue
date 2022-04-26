<template>
  <div class="big">
    <!--inserire contenuto componente-->
    <FilmsComp :propsArrayFilms2="propsArrayFilms" :propsArraySeries2="propsArraySeries"/>
  </div>
</template>

<script>
import FilmsComp from './partials/FilmsComp.vue'

export default {
  //Cambiare il nome con quello del componente creato
  name: 'MainComp',
  components: {
    FilmsComp,
  },
  props: {
    propsArrayFilms: Array,
    propsArraySeries: Array
  }
}
</script>

<style scoped lang="scss">
 /*Inserire style componente*/
 .big{
     height: 80vh;
     background-color: grey;
     overflow: auto;
 }
</style>