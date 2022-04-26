<template>
  <div>
      <div>
          <h5>
              Titolo: {{arrayFilms.title}}
          </h5>
          <h6>
              Titolo originale: {{arrayFilms.original_title}}
          </h6>
          <h6>
              Lingua:
              <span class="flagContainer" :class="(arrayFilms.original_language == 'en') ? 'uk' : (arrayFilms.original_language == 'it' ) ? 'ita' : 'unknown' "></span>
              <!-- {{arrayFilms.original_language}} -->
          </h6>
          <h6>
              Voto: {{arrayFilms.vote_average}}
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

.flagContainer{
    height: 24px;
    width: 24px;
    background-size: contain;
    background-repeat: no-repeat;
    display: inline-block;
}

.ita{
    background-image: url(./../../assets/img/ita.png);
}

.uk{
    background-image: url(./../../assets/img/uk.jpg);
}

.unknown{
    background-image: url(./../../assets/img/unknown.png);
}

</style>