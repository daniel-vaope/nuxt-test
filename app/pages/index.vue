<template>
  <h1>Hola mundo</h1>
  <input v-model="postID" @keydown.enter="openPost" />
</template>

<script setup lang="ts">
const postID = ref("");

function openPost() {
  navigateTo("/blog/" + postID.value);
}
</script>
