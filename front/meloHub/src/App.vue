<script>
import { RouterLink, RouterView } from 'vue-router'
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

  margin: 0 auto;
}
</style>
