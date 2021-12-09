<template>
    <header>
        <div class="container d-flex justify-content-between">
            <ul class="nav">
                <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="#"
                        >Active</a
                    >
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Link</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Link</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link disabled">Disabled</a>
                </li>
            </ul>
            <ul class="nav">
                <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="#"
                        >Active</a
                    >
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Link</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Link</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link disabled">Disabled</a>
                </li>
            </ul>
        </div>

        <div class="container d-flex justify-content-center">
            <div>
                <a href="#">
                    <img src="../assets/avada-food-logo.png" alt="">
                </a>
            </div>
        </div>

        <div class="container_small">
            <nav>
                <ul class="d-flex justify-content-center">
                    <li>
                        PROVA
                    </li>
                    <li>
                        PROVA
                    </li>
                    <li>
                        PROVA
                    </li>
                    <li>
                        PROVA
                    </li>
                    <li>
                        PROVA
                    </li>
                    <li>
                        PROVA
                    </li>
                    <li>
                        PROVA
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header",
};
</script>

<style scoped lang="scss">
.container_small {
    width: 700px;
    margin: 0 auto;
}

ul {
    list-style: none;
    li {
        padding: 0 2rem;
    }
}
</style>
