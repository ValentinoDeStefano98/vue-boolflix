<template>
  <div>
      <div>
          <h5>
              Titolo: {{arrayFilms.title}}
          </h5>
          <h6>
              Titolo originale: {{arrayFilms.original_title}}
          </h6>
      </div>
  </div>
</template>

<script>
export default {
  //Cambiare il nome con quello del componente creato
  name: 'FilmsCard',
  props: {
      arrayFilms: Object
  }
}
</script>

<style scoped lang="scss">
 /*Inserire style componente*/

</style>