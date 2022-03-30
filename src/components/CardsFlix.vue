<template>
    <div class="card">
        <img :src="imgPath" alt="">
        <h2>{{filmElement.title}}</h2>
        <h3>{{filmElement.original_title}}</h3>
        <small>{{filmElement.original_language}}</small>
        <small>{{filmElement.vote_average}}</small>
    </div>
</template>

<script>
export default {
    name:'CardsFlix',
    data(){
        return{
            imgPath: 'https://image.tmdb.org/t/p/w500' + this.filmElement.poster_path
        }
    },
    props:{
    filmElement: Object,
  },
}
</script>

<style lang="scss" scoped>

.card{
    background-color: lightblue;
    border: 1px solid black;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 600px;
    width: 300px;
    img{
        width: 200px;
    }
}

</style>