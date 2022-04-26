<template>
  <div class="big">
    <!--inserire contenuto componente-->
    
  </div>
</template>

<script>
export default {
  //Cambiare il nome con quello del componente creato
  name: 'MainComp',
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