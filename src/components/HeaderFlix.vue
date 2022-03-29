<template>
  <header>
      <div>
          <h1>BOOLFLIX</h1>
      </div>
      <div>
          <input type="text" 
          placeholder="Inserisci il nome:" name="searchInput" id="searchInput"
          value="">
          <button>Cerca</button>
      </div>
  </header>
</template>

<script>
export default {
    name:'HeaderFlix',
}
</script>

<style lang="scss" scoped>
header{
    background-color: lightgray;
}
</style>

