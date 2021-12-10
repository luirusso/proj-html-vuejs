<template>
    <main>
        <div class="container white pb-5 position-relative">
            <div
                class="d-flex pb-4 justify-content-space-between align-items-center"
            >
                <hr />
                <div class="title_spacing flex-grow-1 text-center">
                    <div class="fs-5 fw-600">FOODIE JOURNAL</div>
                </div>
                <hr />
            </div>
            <div
                class="row site_card d-flex text-center justify-content-center"
            >
                <!-- CARD -->
                <div
                    class="card-site col-4"
                    v-for="(element, index) in foodieJournalArray"
                    :key="`foodieJournal-${index}`"
                >
                    <Card
                        :card_image="element.card_image"
                        :card_title="element.card_title"
                        :card_author="element.card_author"
                        :card_date="element.card_date"
                    />
                </div>
            </div>
        </div>

        <div class="container_divider pb-4">
            <SectionDivider
                :title="`POPULAR RECIPES`"
                :text="`Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.`"
            />
        </div>

        <div class="container pb-5">
            <div class="row">
                <div class="col-6 white">
                    <div class="w-100 position-relative">
                        <HoverLink />
                        <img
                            class="w-100"
                            src="../assets/Yogurt-Nan-600x395.jpg"
                            alt=""
                        />
                    </div>
                    <div class="px-5 py-4">
                        <div>
                            <h4 class="title-font">
                                Lunch Favourite with Salad, Naan And Beans
                            </h4>
                            <div class="pb-1">
                                Bakery, Featured, Healthy, Latest Recipes, Staff
                                Picks
                            </div>
                        </div>
                        <div class="pb-1">
                            <hr class="w-100" />
                        </div>
                        <p class="pb-3 fs-6">
                            Suspendisse at semper odio. Nam fringilla
                            scelerisque tincidunt. Orci varius natoque penatibus
                            et magnis dis parturient montes, nascetur ridiculus
                            mus. Donec tincidunt posuere ornare. Phasellus
                            placerat odio non feugiat sollicitudin. Integer
                            vitae elementum ex. Sed porttitor, diam eget
                            convallis volutpat, arcu tellus facilis nulla, id
                            dignissim orci leo id.
                        </p>
                        <span class="button_site">LEARN MORE</span>
                    </div>
                </div>
                <div class="col-6">
                    <div class="row">
                        <div
                            v-for="(popular, index) in popularFoodArray"
                            :key="`popular-${index}`"
                            class="col-6 pb-4 pe-2"
                        >
                            <!-- POPULAR FOOD CARDS -->
                            <div
                                class="popular-food-card overflow-hidden w-100"
                            >
                                <!-- <div class="hover-link">
                                    <div>
                                        <i class="fas fa-link"></i>
                                    </div>
                                    <div>
                                        Fruit Platter with Banana, Mango,
                                        Berries and Orange
                                    </div>
                                </div> -->
                                <div class="position-relative">
                                    <HoverLink />
                                    <img
                                        :src="
                                            require(`../assets/${popular.popularImage}`)
                                        "
                                        alt=""
                                    />
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="container_divider pt-4 pb-3">
            <SectionDivider
                :title="`CULINARY COLLECTION`"
                :text="`Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.`"
            />
        </div>

        <div class="container pb-5">
            <div class="row pb-5">
                <div
                    class="culinary-card col-3 mb-5"
                    v-for="(collection, index) in culinaryCollectionArray"
                    :key="`culinary-${index}`"
                >
                    <CulinaryCollections
                        :image="collection.image"
                        :button="collection.button"
                    />
                </div>
            </div>
        </div>
    </main>
</template>

<script>
import Card from "./Card.vue";
import SectionDivider from "./SectionDivider.vue";
import HoverLink from "./HoverLink.vue";
import CulinaryCollections from "./CulinaryCollections.vue";

export default {
    name: "Main",
    components: {
        Card,
        SectionDivider,
        HoverLink,
        CulinaryCollections,
    },

    data() {
        return {
            foodieJournalArray: [
                {
                    card_image: "single-post-img3-400x263.jpg",
                    card_title:
                        "Food Corner: Top Japanese Restaurants for Sushi",
                    card_author: "By admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-roundup-400x263.jpg",
                    card_title:
                        "Roundup: My New Favourite Recipes For Healthy Living",
                    card_author: "By admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-toasts-400x263.jpg",
                    card_title: "Why These Toasts with Tea are My New Favorite",
                    card_author: "By admin",
                    card_date: "March 25th, 2019",
                },
            ],
            popularFoodArray: [
                {
                    popularImage: "Mixed-fruits-400x263.jpg",
                },
                {
                    popularImage:
                        "r-rachel-park-366508-unsplash-min-400x263.jpg",
                },
                {
                    popularImage:
                        "r-michelle-tsang-500721-unsplash-min-400x263.jpg",
                },
                {
                    popularImage: "quick-summer-drink-460x295.jpg",
                },
                {
                    popularImage:
                        "r-maarten-van-den-heuvel-400626-unsplash-min-460x295.jpg",
                },
                {
                    popularImage: "perfect-cosmopolitan-460x295.jpg",
                },
                {
                    popularImage: "fi2x-6-460x295.jpg",
                },
                {
                    popularImage:
                        "r-brooke-lark-96398-unsplash-min-460x295.jpg",
                },
            ],
            culinaryCollectionArray: [
                {
                    image: "drinks-recipes.png",
                    button: "DRINKS",
                },
                {
                    image: "soups-recipes.png",
                    button: "SOUPS",
                },
                {
                    image: "baking-recipes.png",
                    button: "BAKERY",
                },
                {
                    image: "dinner-recipes.png",
                    button: "DINNER",
                },
                {
                    image: "healthy-recipes.png",
                    button: "HEALTHY",
                },
                {
                    image: "staff-picks.png",
                    button: "STAFF PICKS",
                },
                {
                    image: "premium-recipes.png",
                    button: "APPETISERS",
                },
                {
                    image: "quick-easy-recipes.png",
                    button: "QUICK & EASY",
                },
            ],
        };
    },
};
</script>

<style scoped lang="scss">
@import "../styles/globals.scss";
hr {
    width: calc(100% / 3);
}

.card-site {
    overflow: hidden;
}

.container.white {
    box-shadow: 0px 0px 7px 0px #0000002e, 0px 0px 0px 0px rgb(0 0 0 / 0%);
    padding: 2rem 2rem;
    top: -70px;
}

.popular-food-card {
    max-height: 177px;
    img {
        object-fit: cover;
        width: 100%;
    }
}
</style>
