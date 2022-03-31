<template>
    <div class="card">
        <img id="imgPoster" :src="imgPath" alt="">
        <!-- <img :src="backupImgPath" alt=""> --> <!-- Mi serve per dopo -->
        <h2>{{filmElement.title}}</h2>
        <h3>{{filmElement.original_title}}</h3>
        <img id="flagPoster"
        v-if="this.filmElement.original_language === 'en'"
        :src='langFlagFix'>
        <img id="flagPoster"
        v-else
        :src='this.langFlag'>
        <small>{{filmElement.vote_average}}</small>
    </div>
</template>

<script>
export default {
    name:'CardsFlix',
    data(){
        return{
            langFlag: 'https://countryflagsapi.com/png/' + this.filmElement.original_language,
            langFlagFix: 'https://countryflagsapi.com/png/us',
            imgPath: 'https://image.tmdb.org/t/p/w500' + this.filmElement.poster_path,
            /* backupImgPath: 'https://image.tmdb.org/t/p/w500' + this.filmElement.backdrop_path */  /* Mi serve per dopo */
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
    position: relative;
    #imgPoster{
        width: 200px;
    }
    #flagPoster{
        width: 50px;
        position: absolute;
        top:0;
        left:0;
    }
}

</style>