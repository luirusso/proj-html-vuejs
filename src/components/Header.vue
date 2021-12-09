<template>
    <header>
        <div class="py-3 container d-flex justify-content-between">
            <ul class="nav topnav">
                <li class="nav-item">
                    <div class="d-flex align-items-center">
                        <a class="nav-link download" aria-current="page" href="#"
                            >Download App</a
                        >
                        <span class="button_site"> iOS </span>
                    </div>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Advertise with us</a>
                </li>
            </ul>
            <ul class="nav">
                <li class="nav-item">
                    <a class="nav-link" href="#"
                        ><i class="fab fa-facebook-f"></i
                    ></a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#"
                        ><i class="fab fa-instagram"></i
                    ></a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#"
                        ><i class="fab fa-twitter"></i
                    ></a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#"
                        ><i class="fab fa-youtube"></i
                    ></a>
                </li>
            </ul>
        </div>

        <div class="container pb-4 d-flex justify-content-center">
            <div>
                <a href="#">
                    <img src="../assets/avada-food-logo.png" alt="" />
                </a>
            </div>
        </div>

        <div class="container_small">
            <nav>
                <ul class="d-flex justify-content-center">
                    <li>
                        <a href="#">PROVA</a>
                    </li>
                    <li>
                        <a href="#">PROVA</a>
                    </li>
                    <li>
                        <a href="#">PROVA</a>
                    </li>
                    <li>
                        <a href="#">PROVA</a>
                    </li>
                    <li>
                        <a href="#">PROVA</a>
                    </li>
                    <li>
                        <a href="#">PROVA</a>
                    </li>
                    <li>
                        <a href="#">PROVA</a>
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

.topnav {
    font-size: 11px;
    color: $silverChalice;
    .download {
        padding-right: 5px;
    }
    .button_site {
        font-size: 8px;
        background-color: #fc7525;
        padding: 2px 5px;
        color: white;
        border-radius: 3px;
    }
}

nav {
    ul {
        list-style: none;
        li {
            padding: 0 2rem;
        }
    }
}
</style>
