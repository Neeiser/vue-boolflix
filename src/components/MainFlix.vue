<template>
    <main>
        <div class="card"
        v-for="(film, index) in arrFilms" 
        :key="index">
            <h2>{{film.title}}</h2>
        </div>
    </main>
</template>

<script>
export default {
    name:'MainFlix',
    props:{
    arrFilms: Object,
  },
}
</script>

<style lang="scss" scoped>

.card{
    background-color: lightblue;
}

</style>>