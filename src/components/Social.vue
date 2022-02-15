<template>
      <div class="body__profile__icons">
      <fa :icon="['fab', 'linkedin']" /> <fa :icon="['fab', 'whatsapp']" />  <fa :icon="email" /> 
      </div>
</template>

<script>
export default {
    name: "Social"
}
</script>

<style>
        .body__profile__icons {
            font-size: 3em;
        }
</style>