<template>
    <header>
        <div class="py-2 container d-flex justify-content-between">
            <ul class="nav topnav pt-2">
                <li class="nav-item">
                    <div class="d-flex align-items-center">
                        <a
                            class="nav-link text-glow download"
                            aria-current="page"
                            href="#"
                            >Download App</a
                        >
                        <span class="button_site"> iOS </span>
                    </div>
                </li>
                <li class="nav-item">
                    <a class="nav-link text-glow" href="#">Advertise with us</a>
                </li>
            </ul>
            <ul class="nav pt-2">
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
                        <a href="#">Home</a>
                    </li>
                    <li>
                        <a href="#">Recipes</a>
                    </li>
                    <li>
                        <a href="#">Places</a>
                    </li>
                    <li>
                        <a href="#">Blog</a>
                    </li>
                    <li>
                        <a href="#">About</a>
                    </li>
                    <li>
                        <a href="#">Contacts</a>
                    </li>
                    <li>
                        <a href="#"><i class="fas fa-search"></i></a>
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
@import "../styles/globals.scss";

.topnav {
    font-size: 15px;
    color: $small-text-color;
    .download {
        padding-right: 5px;
    }
    .button_site {
        font-size: 8px;
        padding: 2px 5px;
        color: white;
        border-radius: 3px;
    }
}

.nav-link {
    text-decoration: none;
    color: $small-text-color;
}

.container_small {
    nav {
        ul {
            li {
                padding-bottom: 5px;
                border-bottom: 3px solid transparent;
                &:hover {
                    border-bottom: 3px solid $primary-color;
                }
                a {
                    color: $title-text-color;
                    &:hover {
                        color: $primary-color;
                    }
                }
            }
        }
    }
}

nav {
    ul {
        list-style: none;
        li {
            margin: 0 2rem;
        }
    }
}
</style>
