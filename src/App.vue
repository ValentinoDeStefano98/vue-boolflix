<template>
  <div id="app">
    <HeaderComp/>
    <MainComp/>
  </div>
</template>

<script>
//import bootstrap
import "bootstrap"
import axios from 'axios';


import HeaderComp from './components/HeaderComp.vue'
import MainComp from './components/MainComp.vue'

export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp
  },
  data(){
    return{
      api_key: '4048103a1557792906164decde399a31'
    }    
  },
  created() {
    axios.get( 'https://api.themoviedb.org/3/search/movie?api_key=4048103a1557792906164decde399a31&language=en-US&page=1&include_adult=false&query=rick')
      .then ((res) => {
        console.log(res.data.results);
      }),
    axios.get( 'https://api.themoviedb.org/3/search/tv?api_key=4048103a1557792906164decde399a31&language=en-US&page=1&include_adult=false&query=rick')
      .then ((res) => {
        console.log(res.data.results);
      })
  }
}
</script>

<style lang="scss">
//import bootstrap
@import "bootstrap/dist/css/bootstrap.min.css";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

html{
  max-width: 1440px;
  margin: 0 auto;
}

</style>
