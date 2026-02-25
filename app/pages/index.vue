<template>
  <h1>Hola mundo</h1>
  <input v-model="postID" @keydown.enter="openPost"/>
  <button @click="openPost">Go to post {{ postID }}</button>
</template>

<script setup>

const postID = ref("");

function openPost() {
    navigateTo('/blog/' + postID.value)
}

</script>
