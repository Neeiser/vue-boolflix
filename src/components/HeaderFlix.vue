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
            <button @click="$emit('search', textUserInput)">
                Cerca
            </button>
        </div>
    </header>
</template>

<script>


export default {
    name:'HeaderFlix',
    data(){
        return{
            textUserInput: '',
            arrResponse: [],
            resultCycle: 0,
        };
    },
}
</script>

<style lang="scss" scoped>
header{
    background-color: lightgray;
}
</style>

