<template>
      <div class="body__profile__icons">
      <a href="https://www.linkedin.com/in/gabrielaalvescosta"><fa :icon="['fab', 'linkedin']" /></a> 
      <a href="https://api.whatsapp.com/send?phone=5511957914246"><fa :icon="['fab', 'whatsapp']" /></a>
      <a href="mailto:gabrielaaalvescosta@gmail.com"><fa :icon="['fab', 'google']" /></a>
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
            font-size: 3.5em;
            letter-spacing: 0.40em;
            top: -20px;
            color: #737373;
            position: relative;
        }

        .body__profile__icons a {
            font-size: inherit;
            padding: 0 0.15em;
            color: #737373;
            transition: all 0.5s;
        }

        .body__profile__icons a:hover {
            font-size: inherit;
            color: #ddd;
        }

</style>