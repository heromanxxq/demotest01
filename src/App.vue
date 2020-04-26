<template>
  <div id="app">
    <Tabbar></Tabbar>
  </div>
</template>

<script>
import Tabbar from'./components/tabbar'
export default {
  name: 'App',
  components: {
    Tabbar
  }
}
</script>

<style>
@import './assets/css/base.css';
</style>
