<template>
    <header>
        <div>
            <h1>BOOLFLIX</h1>
        </div>
        <div>
            <input type="text"
            @keyup.enter="$emit('search', textUserInput)"
            placeholder="Inserisci il nome:" 
            name="searchInput" 
            id="searchInput" 
            v-model="textUserInput">
        </div>
    </header>
</template>

<script>


export default {
    name:'HeaderFlix',
    data(){
        return{
            textUserInput: '',
        };
    },
}
</script>

<style lang="scss" scoped>
@import '../assets/partials/variables';

header{
    background-color: $blackFlix;
    display: flex;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100px;
    padding: 0px 20px;
    h1{
        color: $redFlix;
    }
    #searchInput{
        height: 50px;
        padding: 5px;
    }
}
</style>

