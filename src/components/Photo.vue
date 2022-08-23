<template>
    <div class="body__profile__photo">
    <img :src="require('../assets/daniel.jpg')" alt="Perfil" />   
    </div>
</template>

<script>
export default {
    name: "Photo"
}
</script>

<style>
    .body__profile__photo img {
        border-radius: 25%;
        width: 200px;
        height: 200px;
        border: 15px solid #ffcc33 ;
        top: -100px;
        position: relative;
        
    }
</style>

