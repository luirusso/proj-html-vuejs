<template>
    <div class="container pt-4">
        <div class="row pb-5 align-items-center">
            <div class="col-3 border-dot align-self-start pb-5">
                <div class="pb-5">
                    <a href="#"
                        ><img src="../assets/avada-food-logo-mob-2x.png" alt=""
                    /></a>
                </div>
                <div class="d-flex fs-5 pb-3">
                    <!-- <div class="pe-3">
                        <a class="text-glow" href="#"
                            ><i class="fab fa-facebook-f"></i
                        ></a>
                    </div>
                    <div class="pe-3">
                        <a class="text-glow" href="#"
                            ><i class="fab fa-instagram"></i
                        ></a>
                    </div>
                    <div class="pe-3">
                        <a class="text-glow" href="#"
                            ><i class="fab fa-twitter"></i
                        ></a>
                    </div>
                    <div class="pe-3 pb-2">
                        <a class="text-glow" href="#"
                            ><i class="fab fa-youtube"></i
                        ></a>
                    </div> -->

                    <div
                        v-for="(social, index) in socials"
                        :key="`social-${index}`"
                        class="pe-3 pb-2"
                    >
                        <i class="text-glow social-icon" :class="social.icon"></i>
                    </div>
                </div>
            </div>
            <div class="col-3 border-dot pb-4">
                <ul class="footer-links">
                    <li
                        class="pb-3 fs-5"
                        v-for="(link, index) in footerLinks"
                        :key="`link-${index}`"
                    >
                        <a class="text-glow" href="#">{{ link.link }}</a>
                    </li>
                </ul>
            </div>
            <div class="col-3 border-dot pb-2">
                <ul class="pe-4">
                    <li class="pb-4">
                        <h5 class="fw-bold primary">CONTACT</h5>
                    </li>
                    <li
                        v-for="(contact, index) in contacts"
                        :key="`contact-${index}`"
                        class="d-flex fs-5 pb-3"
                    >
                        <div class="pe-3">
                            <i :class="contact.icon"></i>
                        </div>
                        <div>
                            {{ contact.text }}
                        </div>
                    </li>
                </ul>
            </div>
            <div class="col-3 px-4">
                <h5 class="fw-bold primary pb-5">GET OUR APP!</h5>
                <div>
                    <div
                        class="w-100 pt-2 pb-4"
                        v-for="(store, index) in stores"
                        :key="`store-${index}`"
                    >
                        <a href="#"
                            ><img
                                class="download"
                                :src="require(`../assets/${store.store}`)"
                                alt=""
                        /></a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Footer",
    data() {
        return {
            footerLinks: [
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
                    link: "Contact",
                },
            ],
            contacts: [
                {
                    icon: "fas fa-map-marker-alt",
                    text: "775 New York Ave, Brooklyn, Kings, New York 11203",
                },
                {
                    icon: "fas fa-phone",
                    text: "+ 0100-505-0000",
                },
                {
                    icon: "fas fa-envelope",
                    text: "info@your-domain.com",
                },
            ],
            stores: [
                {
                    store: "download-android.png",
                },
                {
                    store: "download-app-store.png",
                },
            ],
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
                {
                    icon: "fab fa-pinterest-p",
                },
            ],
        };
    },
};
</script>

<style scoped lang="scss">
@import "../styles/globals.scss";

ul {
    list-style: none;
}

a {
    color: black;
}

h5 {
    letter-spacing: 3px;
}

.border-dot {
    border-right: 2px dotted lightgray;
}

.social-icon {
    color: rgb(141, 141, 141);
}

.download {
    width: 70%;
}
</style>
