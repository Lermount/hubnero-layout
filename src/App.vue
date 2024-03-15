<template>
  <div id="app" class="container">
    <Aside />
    <div class="dashboard">
      <Header />
      <Main />
    </div>
  </div>
</template>

<script>
import Aside from '@/components/aside/aside-menu.vue';
import Header from '@/components/header/top-panel.vue';
import Main from '@/components/main/main-menu.vue';

export default {
  name: 'App',
  components: {
    Aside,
    Header,
    Main
  }
}
</script>

<style>
#app {
  display: flex;
}

.dashboard {
  width: calc(100% - 72px);
}

@media(max-width: 600px) {
  .dashboard {
    width: 100%;
  }
}
</style>
