<template>
  <h1>Hola mundo</h1>

  <table>
    <thead>
      <tr>
        <th>Nombre</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(item, index) in pokemons" :key="index">
        <td>{{ item.name }}</td>
        <td>
          <NuxtLink to="/">Ver más</NuxtLink>
        </td>
      </tr>
    </tbody>
  </table>
</template>

<script setup>
import axios from "axios";

const pokemons = ref([]);

onMounted(() => {
  axios.get("https://pokeapi.co/api/v2/pokemon").then((res) => {
    pokemons.value = res.data.results;
  });
});
</script>
