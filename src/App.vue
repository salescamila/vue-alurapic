<template>
  <div>
    <h1>{{ titulo }}</h1>
    <h2 v-text="subtitulo"></h2>
    <img :src="foto.url" v-bind:alt="foto.titulo">
  </div>
</template>

<script>
export default {
  data() {
    return {
      titulo: 'Alurapic',
      subtitulo: 'Gatinhos',
      foto: {
        url: 'http://placekitten.com/600/300',
        titulo: 'Kitty'
      }
    }
  }
}
</script>

<style>
</style>
