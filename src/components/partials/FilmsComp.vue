<template>
  <div>
      <h2>Film</h2>
      <FilmsCard v-for="(elem, index) in propsArrayFilms2" :key="index" :arrayFilms="elem"/>
      <h2>TV Series</h2>
      <SeriesCard v-for="(elem, index) in propsArraySeries2" :key="index" :arraySeries="elem"/>
  </div>
</template>

<script>
import FilmsCard from './FilmsCard'
import SeriesCard from './SeriesCard'
export default {
  //Cambiare il nome con quello del componente creato
  name: 'FilmsComp',
  components: {
      FilmsCard,
      SeriesCard
  },
  props: {
    propsArrayFilms2: Array,
    propsArraySeries2: Array
  }
}
</script>

<style scoped lang="scss">
 /*Inserire style componente*/

</style>