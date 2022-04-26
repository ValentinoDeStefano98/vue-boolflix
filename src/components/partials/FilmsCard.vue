<template>
  <div class="col py-3">
      <div class="border bg-dark text-white p-3">
          <!-- Titolo -->
          <!-- <h4>{{arrayFilms.title}}</h4> -->
          <!-- Titolo originale -->
          <!-- <h6>{{arrayFilms.original_title}}</h6> -->
          <!-- Lingua del contenuto -->
          <!-- <div class="d-flex justify-content-center align-items-center">
              <span>Lingua:</span>
              <span class="flagContainer" :class="(arrayFilms.original_language == 'en') ? 'uk' : (arrayFilms.original_language == 'it' ) ? 'ita' : 'unknown' "></span>
          </div> -->
          <img :src="`https://image.tmdb.org/t/p/w342${arrayFilms.poster_path}`" alt="">
          <!-- Voto del contenuto -->
          <!-- <div>
            <i class="fa-solid fa-star" :class="changeScore() >= 1 ? 'text-warning' : ''"></i>
            <i class="fa-solid fa-star" :class="changeScore() >= 2 ? 'text-warning' : ''"></i>
            <i class="fa-solid fa-star" :class="changeScore() >= 3 ? 'text-warning' : ''"></i>
            <i class="fa-solid fa-star" :class="changeScore() >= 4 ? 'text-warning' : ''"></i>
            <i class="fa-solid fa-star" :class="changeScore() == 5 ? 'text-warning' : ''"></i> 
          </div> -->
          
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