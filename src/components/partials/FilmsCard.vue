<template>
  <div class="col py-3">
      <div class="border bg-dark text-white p-3">
          <!-- Titolo -->
          <h4>{{arrayFilms.title}}</h4>
          <!-- Titolo originale -->
          <h6>{{arrayFilms.original_title}}</h6>
          <!-- Lingua del contenuto -->
          <div class="d-flex justify-content-center align-items-center">
              <span>Lingua:</span>
              <span class="flagContainer" :class="(arrayFilms.original_language == 'en') ? 'uk' : (arrayFilms.original_language == 'it' ) ? 'ita' : 'unknown' "></span>
          </div>
          <!-- Voto del contenuto -->
          <span>Voto: {{changeScore()}} </span>
      </div>
  </div>
</template>

<script>
export default {
  //Cambiare il nome con quello del componente creato
  name: 'FilmsCard',
  props: {
      arrayFilms: Object
  },
  methods: {
      changeScore() {
          let score = parseInt(this.arrayFilms.vote_average);
          return parseInt(score / 2);
      }
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