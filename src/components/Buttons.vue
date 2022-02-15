<template>
<div id="demo">
        <div v-if="portugues" class="body__profile__button-area" id="pt-br">
          <transition name="fade" v-on:enter="enter">
                <Portuguese />
                 </transition>
                <Social />
                <button class="body__profile__button github"><a href="https://www.github.com/gabrielaalvescosta">Ver portfólio no GitHub</a></button>
                <button class="body__profile__button cv"><a v-bind:href="curriculo">Baixar Currículo em PDF</a></button>
         
        </div>
        
        <div v-else class="body__profile__button-area">
          <transition name="fade" v-on:enter="enter">
                <English/>
                </transition>
                <Social />
                <button class="body__profile__button github botao"><a href="https://www.github.com/gabrielaalvescosta">View portfolio on GitHub</a></button>
                <button class="body__profile__button cv botao"><a v-bind:href="resume">Download Resume in PDF </a></button>
               
        </div>
        <div class="body__profile__translate">
                <button @click="translate" v-if="trans" v-on:click="fadeMe"><fa icon="flag" /> Translate {{ enFlag }}</button>
                <button @click="translate" v-else v-on:click="fadeMe"><fa icon="flag" /> Traduzir (PT) </button>
        </div>
        </div>
</template>

<script>
import Portuguese from './Portuguese';
import English from './English';
import Social from './Social';

export default {
    
    name: "Buttons",
    el: '#demo',
    components: {
      Portuguese,
      English,
      Social,
    },
    data() {
      return {
        trans: Boolean(true),
        portugues: Boolean,
        resume: "https://github.com/gabrielaalvescosta/gabrielaalvescosta/raw/main/resumes/gabriela-costa-software-engineer-en.pdf",
        curriculo: "https://github.com/gabrielaalvescosta/gabrielaalvescosta/raw/main/resumes/gabriela-costa-software-engineer-pt-br.pdf",
        ptFLag: "(PT-BR)",
        enFlag: "(EN)",
        show: false
      }
    },
    methods: {
      translate() {
        this.portugues = !this.portugues;
        this.trans = !this.trans
        console.log("clicado aqui")
      
      },

      fadeMe: function() {
          this.show = !this.show;
      },

      enter: function() {
          var that = this;
          
          setTimeout(function() {
            that.show = false;
          }, 3000); // hide the message after 3 seconds
      }
    },
    
    
}
</script>

<style>
    .img-anim-enter-active, .img-anim-leave-active {
      transition: transform 0.5s ease, opacity 0.5s ease;
    }
    .img-anim-enter, .img-anim-leave-to {
      transform: translateX(-100px) rotateZ(90deg);
      opacity: 0;
    }
    .anim-img-enter-to, .anim-img-leave {
      transform: translateX(0px) rotateZ(0deg);
      opacity: 1;
    }

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