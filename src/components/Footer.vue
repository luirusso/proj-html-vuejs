<template>
    <div class="container pt-4">
        <div class="row pb-5">
            <div class="col-3 border-dot">
                <div class="pb-5">
                    <a href="#"><img src="../assets/avada-food-logo-mob-2x.png" alt="" /></a>
                </div>
                <div class="d-flex fs-5">
                    <div class="pe-3">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                    </div>
                    <div class="pe-3">
                        <a href="#"><i class="fab fa-instagram"></i></a>
                    </div>
                    <div class="pe-3">
                        <a href="#"><i class="fab fa-twitter"></i></a>
                    </div>
                    <div class="pe-3">
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
            </div>
            <div class="col-3 border-dot">
                <ul class="footer-links">
                    <li class="pb-3 fs-5" v-for="(link, index) in footerLinks" :key="`link-${index}`">
                        <a href="#">{{ link.link }}</a>
                    </li>
                </ul>
            </div>
            <div class="col-3"></div>
            <div class="col-3"></div>
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
                    icon: 'class="fas fa-map-marker-alt"',
                    text: '775 New York Ave, Brooklyn, Kings, New York 11203'
                },
                {
                    icon: '',
                    text: '+ 0100-505-0000'
                },
                {
                    icon: '',
                    text: 'info@your-domain.com'
                },
            ]
        };
    },
};
</script>

<style scoped lang="scss">
ul {
    list-style: none;
}

a {
    color: black;
}

.border-dot {
    border-right: 2px dotted lightgray;
}
</style>
