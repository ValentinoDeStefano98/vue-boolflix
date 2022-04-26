<template>
  <div>
       <div>
          <h5>
              Titolo: {{arraySeries.name}}
          </h5>
          <h6>
              Titolo originale: {{arraySeries.original_name}}
          </h6>
      </div>
  </div>
</template>

<script>
export default {
  //Cambiare il nome con quello del componente creato
  name: 'SeriesCard',
  props: {
      arraySeries: Object
  }
}
</script>

<style scoped lang="scss">
 /*Inserire style componente*/

</style>