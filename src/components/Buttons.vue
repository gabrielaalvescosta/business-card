<template>
        <div v-if="portugues" class="body__profile__button-area">
                <button class="body__profile__button github"><a href="https://www.github.com/gabrielaalvescosta">Ver portfólio no GitHub</a></button>
                <button class="body__profile__button cv"><a v-bind:href="curriculo">Baixar Currículo em PDF</a></button>
        </div>
        <div v-else class="body__profile__button-area">
                <button class="body__profile__button github"><a href="https://www.github.com/gabrielaalvescosta">View portfolio on GitHub</a></button>
                <button class="body__profile__button cv"><a v-bind:href="resume">Download Resume in PDF </a></button>
        </div>
        <div class="body__profile__translate">
                <button @click="translate" v-if="portugues"><fa icon="flag" /> Translate {{ en }}</button>
                <button @click="translate" v-else><fa icon="flag" /> Traduzir {{ pt }}</button>
        </div>
</template>

<script>
export default {
    name: "Buttons",
    data() {
      return {
        portugues: false,
        resume: "https://github.com/gabrielaalvescosta/gabrielaalvescosta/raw/main/resumes/gabriela-costa-software-engineer-en.pdf",
        curriculo: "https://github.com/gabrielaalvescosta/gabrielaalvescosta/raw/main/resumes/gabriela-costa-software-engineer-pt-br.pdf",
        pt: "(PT-BR)",
        en: "(EN)"
      }
    },
    methods: {
      translate() {
        this.portugues = !this.portugues
        console.log("clicado")
      }
    }
}
</script>

<style>
    
    .body__profile__button-area {
      top: -40px;
      position: relative;
    }

    .body__profile button a {
      text-decoration: none;
      color: white;
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
      cursor: pointer;
      transition: all 0.5s;
    }

    .github {
      background-color: #d1a1f5;
    }

    .github:hover {
       background-color: #df2fe6;
    }

    .cv {
      background-color: #b9a9ff;
    }

    .cv:hover {
       background-color: #842fe6;
    }

    .body__profile__translate button {
      font-size: 0.75em;
      border: 0;
      background-color: transparent;
      padding: 0;
      text-transform: uppercase;
      letter-spacing: 3px;
      color: #999;
      top: -10px;
      cursor: pointer;
      position: relative;
      transition: all 0.5s;
    }
    

</style>