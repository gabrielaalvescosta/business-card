<template>
        <button class="body__profile__button github">Ver portfólio no GitHub</button>
      <button class="body__profile__button cv">Baixar Currículo</button>
</template>

<script>
export default {
    name: "Buttons"
}
</script>

<style>
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

</style>