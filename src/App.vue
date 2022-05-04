<template>
  <div id="app">
      <app-header/>

      <main>
          <main-grid/>
          <main-blue-component/>
      </main>

      <app-footer/>
  </div>
</template>

<script>

import AppHeader from './components/AppHeader.vue'
import AppFooter from './components/AppFooter.vue'
import MainGrid from './components/MainGrid.vue'
import MainBlueComponent from './components/MainBlueComponent.vue'

export default {
  name: 'App',
  components: {
    AppFooter,
    AppHeader,
    MainGrid,
    MainBlueComponent,
  }
}
</script>

<style lang="scss">
    @import './style/variables';
    @import './style/general';

</style>
