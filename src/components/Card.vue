<template>
  <div class="body__container">  
  <div class="body__profile">
    <Photo/>
    <Buttons/>
  </div>
  </div>
</template>

<script>

import Photo from './Photo';
import Buttons from './Buttons';

export default {
  name: 'Card',
  components: {
    Photo,
    Buttons,
  },
  methods: {
    translateBio() {
    }
  }
}
</script>

<style>

    .body__container { 
        margin: 0 auto;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .body__profile {
        background: rgb(68, 68, 68);
        border: 3px solid #ff9933;
        box-shadow: rgba(124, 137, 139, 0.12) 0px 2px 4px 0px, rgba(124, 137, 139, 0.32) 0px 2px 16px 0px;
        border-radius: 10px;
        padding: 1.5em 1.75em;
        margin: 2em auto;
        max-width: 330px;
    }
</style>