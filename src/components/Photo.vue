<template>
    <div class="body__profile__photo">
    <img src="../assets/perfil.jpg" alt="Perfil" />   
    </div>
</template>

<script>
export default {
    name: "Photo"
}
</script>

<style>
    .body__profile__photo img {
        border-radius: 50%;
        width: 200px;
        height: 200px;
        border: 15px solid #fff;
        top: -100px;
        position: relative;
        box-shadow: 1px 2px 18px 4px rgb(226, 226, 226);
    }
</style>

