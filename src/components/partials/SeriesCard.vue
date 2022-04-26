<template>
  <div>
       <div>
          <h5>
              Titolo: {{arraySeries.name}}
          </h5>
          <h6>
              Titolo originale: {{arraySeries.original_name}}
          </h6>
          <h6>
              Lingua:
              <span class="flagContainer" :class="(arraySeries.original_language == 'en') ? 'uk' : (arraySeries.original_language == 'it' ) ? 'ita' : 'unknown' "></span>
              <!-- {{arraySeries.original_language}} -->
          </h6>
          <h6>
              Voto: {{arraySeries.vote_average}}
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