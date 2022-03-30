<template>
    <header>
        <div>
            <h1>BOOLFLIX</h1>
        </div>
        <div>
            <input type="text" 
            placeholder="Inserisci il nome:" 
            name="searchInput" 
            id="searchInput" 
            v-model="textUserInput">
            <button @click="startSearchFunction">
                Cerca
            </button>
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
            arrResponse: [],
            resultCycle: 0,
        };
    },
    /* computed(){
        axios.get('https://api.themoviedb.org/3/search/movie?api_key=2a1eafb77e5173892c5f55c2d7d7a8c8&language=it-IT&query=' + this.textUserInput)
        .then(() => {
            
        })
    }, */
    methods:{
        startSearchFunction(){
            axios.get('https://api.themoviedb.org/3/search/movie?api_key=2a1eafb77e5173892c5f55c2d7d7a8c8&language=it-IT&query=' + this.textUserInput)
            .then((item) =>{
                this.arrResponse = item.data.results; /* + [this.resultCycle] */
                console.log(this.arrResponse);
            })
        }
    }
}
</script>

<style lang="scss" scoped>
header{
    background-color: lightgray;
}
</style>

