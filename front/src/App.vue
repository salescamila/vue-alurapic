<template>
  <div class="corpo">
    <nav-menu :rotas="routes"/>

    <transition name="pagina">
      <router-view></router-view>
    </transition>
  </div>
</template>

<script>

import { routes } from './routes';
import Menu from './components/shared/menu/Menu.vue';

export default {
  components: {
    'nav-menu': Menu
  },
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

  .pagina-enter-active, .pagina-leave-active {
    transition: opacity .2s;
  }
  .pagina-enter, .pagina-leave-active {
    opacity: 0;
  }

</style>
