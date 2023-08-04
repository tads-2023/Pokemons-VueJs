<script setup>
import Pokemon from './components/Pokemon.vue';
import { ref } from 'vue';

const pokemons = ref([]);

fetch("https://pokeapi.co/api/v2/pokemon").then( (res) => {
  return res.json();
}).then( (json) => {
  pokemons.value = json.results;
}).catch( (err) => {
  console.log("deu ruim...", err);
})
</script>

<template>
  
  <h1>Pokemons</h1>
  <div v-for="pokemon in pokemons">
    <Pokemon :pokemon="pokemon" />
  </div>
</template>

<style scoped>
</style>
