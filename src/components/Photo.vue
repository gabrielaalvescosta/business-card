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
        width: 250px;
        height: 250px;
        border: 15px solid #fff;
        top: -90px;
        position: relative;
        box-shadow: 1px 2px 18px 4px rgb(226, 226, 226);
    }
</style>

