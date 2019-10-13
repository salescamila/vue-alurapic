<template>
  <div>
    <h1>{{ titulo }}</h1>
    <h2 v-text="subtitulo"></h2>

    <ul>
      <li v-for="foto of fotos" v-bind:key="foto">
        <img :src="foto.url" v-bind:alt="foto.titulo">
      </li>
    </ul>

  </div>
</template>

<script>
export default {
  data() {
    return {
      titulo: 'Alurapic',
      subtitulo: 'Gatinhos',
      fotos: [
        {
        url: 'http://placekitten.com/600/300',
        titulo: 'Kitty'
        },
        {
          url: 'http://placekitten.com/500/300',
          titulo: 'Kitty2'
        }
      ]
    }
  }
}
</script>

<style>
</style>
