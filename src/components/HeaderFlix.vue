<template>
    <header>
        <div>
            <h1>BOOLFLIX</h1>
        </div>
        <div>
            <form @submit.prevent="$emit('searchTitle', textUserInput)">
                <label for="searchInput">
                    <input type="text" 
                    placeholder="Inserisci il nome:" 
                    name="searchInput" 
                    id="searchInput" 
                    v-model="textUserInput">
                    <button>
                        Cerca
                    </button>
                </label>
            </form>
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
header{
    background-color: lightgray;
}
</style>

