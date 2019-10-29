<template>
  <nav>
    <ul class="list-menu">
      <li class="list-menu-item" v-for="rota in rotas" :key="rota">
        <router-link :to="rota.path ? rota.path : '/'">
          {{ rota.titulo }}
        </router-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  props: {
    rotas:{
      type: Array,
      required: true
    }
  }

}
</script>

<style scoped>

  .list-menu-item{
    display:inline-block;
    margin-right: 2%;
  }

</style>