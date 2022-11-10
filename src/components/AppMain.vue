<script>
import { store } from "../store";
import CharacterCard from "./CharacterCard.vue";
export default {
    name: "AppMain",
    components: {
        CharacterCard
    },
    data() {
        return {
            store
        }
    }
}
</script>


<template>
    <div class="container mt-5">
        <div class="results d-flex align-items-center ">
            <h2 class="">Found 62 characters</h2>
        </div>
        <div class="row row-cols-2 row-cols-md-4 mt-5">
            <div class="col" v-for="character in store.characters" :key="character.id">
                <CharacterCard :character="character" />
            </div>
        </div>


    </div>
</template>


<style lang="scss" scoped>
.container {

    background-color: white;
    overflow: scroll;
    height: 800px;



    .results {
        background-color: rgb(41, 39, 39);
        color: white;



    }
}
</style>