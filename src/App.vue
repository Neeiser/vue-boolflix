<template>
  <div id="app">
    <HeaderFlix @search="searchFunction"></HeaderFlix>
    <MainFlix :arrFilms="arrFilms"></MainFlix>
  </div>
</template>

<script>
import HeaderFlix from './components/HeaderFlix.vue'
import MainFlix from './components/MainFlix.vue'
import axios from 'axios';

export default {
  name: 'App',
  data(){
    return{
      arrFilms: [],
    };
  },
  components:{
    HeaderFlix,
    MainFlix,
  },
  methods:{
    searchFunction(argText){
      axios.get('https://api.themoviedb.org/3/search/movie?api_key=2a1eafb77e5173892c5f55c2d7d7a8c8&language=it-IT&query=' + argText)
      .then((item) =>{
          this.arrFilms = item.data.results;
          console.log(this.arrFilms);
      })
    }
  }
}
</script>

<style lang="scss" scoped >

main{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
