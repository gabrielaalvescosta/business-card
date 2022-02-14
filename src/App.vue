<template>
  <Portuguese />
  <English />
</template>

<script>
import English from './components/English.vue'
import Portuguese from './components/Portuguese.vue'

export default {
  name: 'App',
  components: {
    English,
    Portuguese
  }
}
</script>

<style>
@import './app.scss';

#app {
  font-family: Orkney, sans-serif;
  font-weight: bold;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
