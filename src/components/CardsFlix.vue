<template>
    <div class="card">
        <h2>{{filmElement.title}}</h2>
        <h3>{{filmElement.original_title}}</h3>
        <small>{{filmElement.original_language}}</small>
        <small>{{filmElement.vote_average}}</small>
    </div>
</template>

<script>
export default {
    name:'CardsFlix',
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
    height: 400px;
    width: 200px;
    small{

    }
}

</style>>