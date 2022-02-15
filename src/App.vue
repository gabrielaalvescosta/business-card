<template>
  <div class="container">
    <Loading />
  <Card/>
  </div>
</template>

<script>
import Card from './components/Card';
import Loading from './components/Loading';

export default {
  name: 'App',
  components: {
    Card,
    Loading,
  },
}
</script>

<style>
@import './app.scss';

#app {
  font-family: Orkney, sans-serif;
  font-size: 1.2em;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #303030;
  margin-top: 60px;
}
</style>
