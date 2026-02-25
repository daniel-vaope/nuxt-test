<!-- Ruta dinámica dentro de la ruta /blog/{id} -->
<template>
  <!-- Getting ID from route params -->
  <h1>Post {{ $route.params.id }}</h1>
  <button @click="sendParams(123)">Enviar parametros</button>
</template>

<script setup>
function sendParams(id) {
  // Additional logic
  console.log(id);
  // this.$router.push("/blog/" + id);
}

definePageMeta({
  validate(route){
    return publishedPosts.some(p => p.id === route.params.id)
  }
})

const publishedPosts = [
  { id: '1', title: 'Hola mundo'},
  { id: '2', title: 'Aeaaa'}
]

</script>
