<template>
  <div class="corpo">
    <nav>
      <ul class="list-menu">
        <li class="list-menu-item" v-for="route in routes" :key="route">
          <router-link :to="route.path ? route.path : '/'">
            {{ route.titulo }}
          </router-link>
        </li>
      </ul>
    </nav>

    <router-view></router-view>
  </div>
</template>

<script>

import { routes } from './routes';
export default {
  data() {
    return{
      routes
    }
  }
}
</script>

<style scoped>
  .corpo {
    font-family: Helvetica, sans-serif;
    width: 96%;
    margin: 0 auto;
  }
  .list-menu-item{
    display:inline-block;
    margin-right: 2%;
  }
</style>
