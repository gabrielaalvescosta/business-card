<template>
<div id="demo">
        <div v-if="german" class="body__profile__button-area" id="de">
          <transition name="fade" v-on:enter="enter">
                <German />
                 </transition>
                <Social />
                <button class="cta-phone"><a href="tel:+491604732199"><fa :icon="['fa', 'calendar']" /> Termin buchen</a></button>
                <button class="body__profile__button github"><a href="https://www.gallery.danielba.de">Galerie besuchen</a></button>
        </div>
        
        <div v-else class="body__profile__button-area">
          <transition name="fade" v-on:enter="enter">
                <English/>
                </transition>
                <Social />
                <button class="cta-phone"><a href="tel:+491604732199"><fa :icon="['fa', 'calendar']" /> Book a Date</a></button>
                <button class="body__profile__button github botao"><a href="https://www.gallery.danielba.de">Visit Gallery</a></button>
        </div>
        <div class="body__profile__translate">
                <button @click="translate" v-if="trans" v-on:click="fadeMe"><fa icon="flag" /> Translate</button>
                <button @click="translate" v-else v-on:click="fadeMe"><fa icon="flag" /> Übersetzen </button>
        </div>
        </div>
</template>

<script>
import English from './English';
import German from './German';
import Social from './Social';

export default {
    
    name: "Buttons",
    el: '#demo',
    components: {
      English,
      German,
      Social,
    },
    data() {
      return {
        trans: Boolean(true),
        german: Boolean,
        curriculo: "https://www.gallery.danielba.de",
        deFLag: "(DE)",
        enFlag: "(EN)",
        show: false,
      }
    },
    methods: {
      translate() {
        this.german = !this.german;
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
        .fade-enter-active,
    .fade-leave-active {
      transition: opacity 1s
    }

    .fade-enter,
    .fade-leave-to
    /* .fade-leave-active in <2.1.8 */

    {
      opacity: 0
    }

    .body__profile__button-area {
      top: -40px;
      position: relative;
    }

    /* .body__profile button a {
      text-decoration: none;
      color: #666;
    } */

    .body__profile__button {
      border: none;
      border-radius: 10px;
      font-family: Orkney;
      text-transform: uppercase;
      padding: 1.5em 1em;
      width: 100%;
      color: white;
      letter-spacing: 2px;
      font-weight: bold;
      cursor: pointer;
      transition: all 0.5s;
    }

    .body__profile__button a {
      text-decoration: none;
    }

    .cta-phone {
      background: rgb(68, 68, 68);
      border: #ff9933 solid 2px;
      border-radius: 10px;
      font-family: Orkney;
      text-transform: uppercase;
      padding: 1.5em 1em;
      width: 100%;
      color: white;
      letter-spacing: 2px;
      font-weight: bold;
      margin-bottom: 1em;
      cursor: pointer;
      transition: all 0.5s;
    }

    .cta-phone a {
      text-decoration: none;
      color: #ff9933;
    }

    .cta-phone:hover {
      border-color: #ffcc33;
      box-shadow: rgba(124, 137, 139, 0.12) 0px 2px 4px 0px, rgba(124, 137, 139, 0.32) 0px 2px 16px 0px;
    }

    .cta-phone a:hover {
      color: #ffcc33;
      transition: all 0.25s;
    }

    .github {
      background-color: #ff9933;
      color: #666;
    }

    .github:hover {
       background-color: #ffcc33;
       box-shadow: rgba(124, 137, 139, 0.12) 0px 2px 4px 0px, rgba(124, 137, 139, 0.32) 0px 2px 16px 0px;
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