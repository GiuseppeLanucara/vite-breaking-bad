<script>
export default {
    name: "AppHeader"
}
</script>

<template>
    <div class="d-flex align-items-center container-fluid ms-3 mt-4">
        <img class="rounded-circle" src="../assets/img/brba.jpg" alt="">
        <h1 class="ms-3">Breaking Bad API</h1>
    </div>
    <div class="container">
        <nav>
            <div class="dropdown">
                <button class="mt-5 btn ms-color dropdown-toggle" type="button" data-bs-toggle="dropdown"
                    aria-expanded="false">
                    Select Category
                </button>
                <ul class="dropdown-menu">
                    <li><a class="dropdown-item" href="#">Action</a></li>
                    <li><a class="dropdown-item" href="#">Another action</a></li>
                    <li><a class="dropdown-item" href="#">Something else here</a></li>
                </ul>
            </div>
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
</style>