<template>
    <main>
        <CardsFlix
        v-for="film in arrFilms"
        :key="film.id"
        :filmElement="film">
        </CardsFlix>
    </main>
</template>

<script>
import CardsFlix from './CardsFlix.vue'

export default {
    name:'MainFlix',
    components:{
        CardsFlix,
    },
    props:{
        arrFilms: Array
    }
}
</script>

<style lang="scss" scoped>

</style>>