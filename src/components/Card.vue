<template>
  <div class="body__container">  
  <div class="body__profile">
    <Photo/>
    <Bio/>
    <Social/>
    <Buttons/>
  </div>
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

    .body__container { 
      
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .body__profile {
        background: white;
        border-radius: 50px;
        padding: 1.5em 1.75em;
        margin: 2em auto;
        max-width: 330px;
        box-shadow: 0px 3px 136px 0px rgba(88, 87, 119, 0.21);
    }
</style>