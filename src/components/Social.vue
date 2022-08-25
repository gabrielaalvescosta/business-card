<template>
      <div class="body__profile__icons">
      <a href="https://www.instagram.com/daniel.ba.photo/"><fa :icon="['fab', 'instagram']" /></a> 
      <a href="https://api.whatsapp.com/send?phone=491604732199"><fa :icon="['fab', 'whatsapp']" /></a>
      <a href="mailto:d.baptista@me.com"><fa :icon="['fab', 'google']" /></a>
      </div>
</template>

<script>
export default {
    name: "Social"
}
</script>

<style>
        a {
            color: #999;
        }
        .body__profile__icons {
            font-size: 3em;
            letter-spacing: 0.40em;
            top: -20px;
            color: #ff9933;
            position: relative;
            margin-top: 2rem;
            margin-bottom: 1rem;
        }

        .body__profile__icons a {
            font-size: inherit;
            padding: 0 0.15em;
            color: #ff9933;
            transition: all 0.5s;
        }

        .body__profile__icons a:hover {
            font-size: inherit;
            color: #ffcc33;
        }
</style>