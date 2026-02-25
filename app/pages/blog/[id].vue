<!-- Ruta dinámica dentro de la ruta /blog/{id} -->
<template>
  <!-- Getting ID from route params -->
  <h1>Post {{ $route.params.id }}</h1>
  <button @click="sendParams(123)">
    Enviar parametros
  </button>
</template>

<script>
export default {
  methods: {
    sendParams(id) {
      // Additional logic
      console.log(id);
      this.$router.push("/blog/" + id);
    },
  },
};
</script>
