<template>
  <div class="container">
    <h2>Film</h2>
    <div class="row row-cols-3">
        <!-- Card dei film -->
        <FilmsCard v-for="(elem, index) in propsArrayFilms2" :key="index" :arrayFilms="elem"/>
    </div>
    <h2>TV Series</h2>
    <div class="row row-cols-3">
        <!-- Card delle serie tv -->
        <SeriesCard v-for="(elem, index) in propsArraySeries2" :key="index" :arraySeries="elem"/>
    </div>   
  </div>
</template>

<script>
import FilmsCard from './FilmsCard'
import SeriesCard from './SeriesCard'
export default {
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