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
      fotos: []
    }
  },
  created(){
    this.$http.get('http://localhost:3000/v1/fotos')
      .then(res => res.json())
      .then(fotos => this.fotos = fotos, err => console.log(err));
  }
}
</script>

<style>
</style>
