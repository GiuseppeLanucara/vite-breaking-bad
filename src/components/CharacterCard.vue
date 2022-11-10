<script>
export default {
    name: "CharacterCard",
    props: {
        character: Object
    }
}
</script>


<template>
    <div class="character-cart d-flex justify-content-center flex-column">
        <img :src="character.img" alt="">
        <h3>{{ character.name }}</h3>
        <h4>{{ character.category }}</h4>
        <h5>{{ character.status }}</h5>
    </div>

</template>


<style lang="scss" scoped>
.character-cart {
    background-color: rgb(41, 39, 39);
    text-align: center;
    margin-bottom: 30px;
    color: white;
    height: 600px;

    img {
        margin-left: 30px;
        margin-right: 30px;
        margin-top: 20px;
        height: 350px;
    }

    h4 {
        color: grey;
    }

    h5 {
        color: grey;
        font-weight: lighter;
    }
}
</style>