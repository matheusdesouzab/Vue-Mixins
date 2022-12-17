<template>
  <div class="container">
    <div class="row p-4">
      <div class="col">
        <lista-filmes />
      </div>
      <div class="col">
        <lista-pessoas />
      </div>
      <div class="col">
        <lista-videogames />
      </div>
    </div>
  </div>
</template>

<script>

import ListaFilmes from './components/ListaFilmes.vue';
import ListaPessoas from './components/ListaPessoas.vue';
import ListaVideogames from './components/ListaVideogames.vue';

export default {
  name: 'App',
  components: {
    ListaFilmes,
    ListaPessoas,
    ListaVideogames
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
