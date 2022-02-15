<template>
  <div class="container">
  <Card/>
  </div>
</template>

<script>
import Card from './components/Card';

export default {
  name: 'App',
  components: {
    Card,
  }
}
</script>

<style>
@import './app.scss';

#app {
  font-family: Orkney, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #303030;
  margin-top: 60px;
}
</style>
