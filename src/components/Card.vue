<template>
  <div class="body__profile">
    <Photo/>
          <h1>Gabriela Costa</h1>
          <h2>UI/UX designer</h2>
          <h2>Front-end Web Developer</h2>
          <div class="body__profile__bio">Desenvolvedora front-end com
            conhecimentos em HTML, CSS e
            JavaScript, ReactJs e Vue.js. 
            Atualmente aprendendo Java
            e TypeScript.
          </div>
    <Social/>
    <Buttons/>
  </div>
</template>

<script>
import Social from './Social';
import Photo from './Photo';
import Buttons from './Buttons';

export default {
  name: 'Card',
  components: {
    Photo,
    Social,
    Buttons
  }
}
</script>

<style>
    .body__profile {
        background: white;
        border-radius: 20px;
        padding: 2em;
        min-width: 375px;
        margin: 0 auto;
        max-width: 420px;
    }
</style>