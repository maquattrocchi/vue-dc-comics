<template>
  <div id="app">
      <app-header/>

      <main>
          <div>Blocco Nero</div>
          <main-blue-component/>
      </main>
      
      <app-footer/>
  </div>
</template>

<script>

import AppHeader from './components/AppHeader.vue'
import AppFooter from './components/AppFooter.vue'
import MainBlueComponent from './components/MainBlueComponent.vue'

export default {
  name: 'App',
  components: {
    AppFooter,
    AppHeader,
    MainBlueComponent
  }
}
</script>

<style lang="scss">

</style>
