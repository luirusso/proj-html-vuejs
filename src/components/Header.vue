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
                <li
                    v-for="(social, index) in socials"
                    :key="`social-${index}`"
                    class="nav-item"
                >
                    <a class="nav-link text-glow" href="#"
                        ><i :class="social.icon"></i
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
                    <li
                        v-for="(link, index) in navLinks"
                        :key="`link-${index}`"
                    >
                        <a href="#">{{ link.link }}</a>
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
    data() {
        return {
            socials: [
                {
                    icon: "fab fa-facebook-f",
                },
                {
                    icon: "fab fa-instagram",
                },
                {
                    icon: "fab fa-twitter",
                },
                {
                    icon: "fab fa-youtube",
                },
            ],
            navLinks: [
                {
                    link: "Home",
                },
                {
                    link: "Recipes",
                },
                {
                    link: "Places",
                },
                {
                    link: "Blog",
                },
                {
                    link: "About",
                },
                {
                    link: "Contacts",
                },
            ],
        };
    },
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
                transition: all 0.4s ease-in-out;
                &:hover {
                    border-bottom: 3px solid $primary-color;
                }
                a {
                    color: $title-text-color;
                    transition: all 0.4s ease-in-out;
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
