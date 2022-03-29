<template>
  <header>
      <div>
          <h1>BOOLFLIX</h1>
      </div>
      <div>
          <input type="text" 
          placeholder="Inserisci il nome:" name="searchInput" id="searchInput"
          value="" v-model="textUserInput">
          <button>Cerca</button>
      </div>
  </header>
</template>

<script>
import axios from 'axios';

export default {
    name:'HeaderFlix',
    data(){
        return{
            textUserInput: '',
        };
    },
    created(){
        axios.get('https://api.themoviedb.org/3/search/movie?api_key=2a1eafb77e5173892c5f55c2d7d7a8c8&language=it-IT')
        .then
    }
}
</script>

<style lang="scss" scoped>
header{
    background-color: lightgray;
}
</style>

