<template>
  <div class="body__profile">
    <Photo/>
    <Bio/>
    <Social/>
    <Buttons/>
  </div>
</template>

<script>
import Social from './Social';
import Photo from './Photo';
import Bio from './Bio';
import Buttons from './Buttons';

export default {
  name: 'Card',
  components: {
    Photo,
    Social,
    Buttons,
    Bio
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