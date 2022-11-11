<script>
import { store } from "../store";
export default {
    name: "AppHeader",
    data() {
        return {
            store,
            seriesFilter: ["Breaking Bad", "Better Call Saul"]
        }
    }
}
</script>

<template>
    <div class="d-flex align-items-center container-fluid ms-3 mt-4">
        <img class="rounded-circle" src="../assets/img/brba.jpg" alt="">
        <h1 class="ms-3">Breaking Bad API</h1>
    </div>
    <div class="container">
        <nav>
            <div class="form-floating lbl mt-4 mb-5 dp-flex justify-content-center">
                <select class="form-select" id="floatingSelect" aria-label="Floating label select example"
                    v-model="store.seriesStatus">
                    <option selected>Select a Category</option>
                    <option v-for="(serie, index) in seriesFilter" :value="serie" :key="index">{{ serie }}</option>
                </select>
                <label for="floatingSelect"></label>
            </div>
            <button type="button" class="btn btn-primary" @click="$emit("")">Primary</button>
        </nav>
    </div>

</template>


<style lang="scss" scoped>
h1 {
    color: white;
}

.ms-color {
    background-color: white;

    &:hover {
        background-color: white;
    }

}

img {
    max-width: 50px;
}

.lbl {
    width: 20%;
}
</style>