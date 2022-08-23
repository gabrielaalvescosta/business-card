<template>
         
          <div class="body__profile__title">
          <h1>Daniel Baptista</h1>
          <h2>Photographer</h2>
          <h2>Adobe Certified</h2>
          <span class="linebreaker"></span>
          <div class="body__profile__bio-de">{{ bioDe }}
          <span class="linebreaker"></span>
          </div>
          </div>
      
</template>

<script>

export default {
    name: "German",
    data: () => ({

      bioDe: `Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam`

    }),
    
}
</script>

<style>
      .body__profile__title {
        top: -20px;
        position: relative;
      }

      .body__profile__title h1 {
        font-size: 1.5em;
        font-weight: 900;
        text-align: center;
        color: rgb(171, 171, 171);
        text-transform: uppercase;
        margin: 0 0 0.5em 0;
      }

      .body__profile__title h2 {
        font-size: 0.75em;
        color: rgb(153, 153, 153);
        line-height: 1.391;
        font-weight: lighter;
        text-align: center;
        text-transform: uppercase;

      }

      .body__profile__bio-de {
        font-size: 0.75em;
        color: rgb(171, 171, 171);
        font-weight: 900;
        line-height: 1.404;
        text-align: center;
        margin: 1em 0;
        transition:all 0.5s ease-in-out;
      }

      .linebreaker {
        display: inline-block;
        width: 95%;
        height: 2px;
        background-color: #ff9933;
        box-shadow: rgba(124, 137, 139, 0.12) 0px 2px 4px 0px, rgba(124, 137, 139, 0.32) 0px 2px 16px 0px;
      }
</style>

