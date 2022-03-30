<template>
    <main>
        <div class="card">
            <h2>{{filmElement.title}}</h2>
        </div>
    </main>
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
}

</style>>