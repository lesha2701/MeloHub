<script>
import { RouterLink, RouterView } from 'vue-router'
import HomeView from './views/HomeView.vue';

export default {
  components: {
    HomeView
  }
}
</script>

<template>
  <div class="container"> 
    <RouterView />
  </div>
</template>

<style lang="scss">
.container {
  display: flex;
  flex-direction: column;

  max-width: 1440px;
  min-height: 100vh;

  padding: 15px 0;
  margin: 0 auto;
}
</style>
