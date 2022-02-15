<template>
      <div class="body__profile__icons">
      <fa :icon="['fab', 'linkedin']" /> <fa :icon="['fab', 'whatsapp']" />  <fa :icon="['fab', 'google']" /> 
      </div>
</template>

<script>
export default {
    name: "Social"
}
</script>

<style>
        .body__profile__icons {
            font-size: 3.5em;
            letter-spacing: 0.25em;
            top: -60px;
            color: #737373;
            position: relative;
        }
</style>