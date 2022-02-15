<template>
        <div class="body__profile__button-area">
                <button class="body__profile__button github">Ver portfólio no GitHub</button>
                <button class="body__profile__button cv">Baixar Currículo em PDF</button>
        </div>
        <div class="body__profile__translate">
          <fa icon="flag" /> Translate
        </div>
</template>

<script>
export default {
    name: "Buttons"
}
</script>

<style>
    
    .body__profile__button-area {
      top: -40px;
      position: relative;
    }
    .body__profile button {
      border: none;
      border-radius: 10px;
      font-family: Orkney;
      text-transform: uppercase;
      padding: 1.5em 1em;
      width: 100%;
      color: white;
      letter-spacing: 2px;
      font-weight: bold;
      margin: 0.5em 0;

    }

    .github {
      background-color: #d1a1f5;
    }

    .cv {
      background-color: #b9a9ff;
    }

    .body__profile__translate {
      font-size: 0.75em;
      text-transform: uppercase;
      letter-spacing: 3px;
      color: #999;
      top: -10px;
      position: relative;
    }

</style>