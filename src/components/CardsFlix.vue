<template>
    <div class="card">
        <div class="film-poster">
            <img id="imgPoster" :src="imgPath" alt="">
        </div>
        <div class="film-info">
            <h2>{{filmElement.title}}</h2>
            <h3>{{filmElement.original_title}}</h3>
            <small id="film-desc">{{filmElement.overview}}</small>
            <small>{{filmElement.vote_average}}</small>
        </div>
        <img id="flagPoster"
        v-if="this.filmElement.original_language === 'en'"
        :src='langFlagFix'>
        <img id="flagPoster"
        v-else
        :src='this.langFlag'>
        <!-- <img :src="backupImgPath" alt=""> --> <!-- Mi serve per dopo -->
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
        }
    },
    props:{
    filmElement: Object,
    },
}
</script>

<style lang="scss" scoped>
@import '../assets/partials/variables';

.card{
    border: 1px solid $blackFlix;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 450px;
    width: 300px;
    margin: 5px;
    position: relative;
    .film-poster{
    height: 450px;
    width: 300px;
    position: relative;
        #imgPoster{
            width: 200px;
            position: absolute;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
    }
    .film-info{
        display: none;
        h3{
            font-size: 0.8rem;
        }
        #film-desc{
            text-align: center;
        }
    }
    #flagPoster{
        width: 50px;
        border-radius: 5px;
        position: absolute;
        top: 5px;
        left: 5px;
    }
}

.card:hover{
    .film-poster{
    display: none;
    }
    #imgPoster{
        height: 0px;
        transition: 0.3s;
    }
    .film-info{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-evenly;
        padding: 10px;
        height: 450px;
        width: 298px;
        background-color: lightgray;
    }
}



</style>