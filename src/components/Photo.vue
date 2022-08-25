<template>
    <div class="body__profile__photo">
    <img :src="require('../assets/ME.jpg')" alt="Daniel - the author" />   
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
        box-shadow: rgba(124, 137, 139, 0.12) 0px 2px 4px 0px, rgba(124, 137, 139, 0.32) 0px 2px 16px 0px;
        width: 200px;
       
        border: 0.219rem solid #ff9933 ;
        top: -100px;
        position: relative;
        margin-bottom: 1em;
    }

    .body__profile__photo {
        margin-bottom: 0;
        height: 175px;
    }
</style>

