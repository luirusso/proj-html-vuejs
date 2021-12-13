<template>
    <main>
        <FoodieJournal />

        <div class="container_divider pb-4">
            <SectionDivider
                class="text-center"
                :title="`POPULAR RECIPES`"
                :text="`Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.`"
            />
        </div>

        <div class="container pb-5">
            <PopularRecipes />
        </div>

        <div class="container_divider pt-5 pb-3">
            <SectionDivider
                class="text-center"
                :title="`CULINARY COLLECTION`"
                :text="`Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.`"
            />
        </div>

        <div class="container pb-5">
            <div class="row pb-5">
                <div
                    class="culinary-card d-flex justify-content-center align-items-center col-3 mb-5"
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

        <div class="container pb-4">
            <div class="d-flex align-items-center justify-content-between">
                <div class="text-start">
                    <SectionDivider
                        class="text-start w-75"
                        :title="`FARM TO TABLE`"
                        :text="`Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.`"
                    />
                </div>
                <div>
                    <div class="button_site_square small-border py-2 px-4">
                        <span class="pe-2">READ OUR BLOG</span>
                        <span><i class="fas fa-book-reader"></i></span>
                    </div>
                </div>
            </div>
        </div>

        <!-- FOOD CORNER SECTION -->
        <div class="container">
            <div class="row justify-content-between">
                <div class="col-7">
                    <div class="big_card white p-0 pb-4 mb-5 box-shadow">
                        <div class="w-100 position-relative">
                            <HoverLink
                                :linkTitle="`Food Corner: Top Japanese Restaurants for
                                    Sushi`"
                            />
                            <img
                                class="w-100"
                                src="../assets/single-post-img3-800x527.jpg"
                                alt=""
                            />
                        </div>
                        <div class="px-5 py-4">
                            <div>
                                <h4 class="title-font text-glow">
                                    Food Corner: Top Japanese Restaurants for
                                    Sushi
                                </h4>
                                <div class="pb-1">
                                    Bakery, Featured, Healthy, Latest Recipes,
                                    Staff Picks
                                </div>
                            </div>
                            <div class="pb-1">
                                <hr class="w-100" />
                            </div>
                            <p class="pb-3 fs-6">
                                Suspendisse at semper odio. Nam fringilla
                                scelerisque tincidunt. Orci varius natoque
                                penatibus et magnis dis parturient montes,
                                nascetur ridiculus mus. Donec tincidunt posuere
                                ornare. Phasellus placerat odio non feugiat
                                sollicitudin. Integer vitae elementum ex. Sed
                                porttitor, diam eget convallis volutpat, arcu
                                tellus facilis nulla, id dignissim orci leo id.
                            </p>
                            <div class="d-flex justify-content-between">
                                <div class="text-glow">Read more ></div>
                                <div class="text-glow">
                                    <i class="far pe-1 fa-comments"></i>
                                    <span>0</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="col-4">
                    <!-- BIG SIDE CARD LATEST RECIPES -->
                    <div
                        class="latest-recipes-banner d-flex align-items-center justify-content-center mb-5 cursor-pointer"
                    >
                        <div class="w-25 h-25 d-flex">
                            <span class="fs-4 text-center">
                                VIEW OUR LATEST RECIPES
                            </span>
                        </div>
                    </div>
                    <div class="row">
                        <!-- SINGAPORE CITY GUIDE -->
                        <div class="col-12">
                            <div class="singapore-guide cursor-pointer">
                                <div>
                                    <div class="guide-text fs-3">
                                        City Guide: Singapore
                                    </div>
                                </div>
                            </div>
                            <div class="button_site_square text-center">
                                <span>
                                    <i class="fas fa-globe-americas"></i>
                                    VIEW ALL CITY GUIDES
                                </span>
                            </div>
                        </div>
                        <div class="py-4">
                            <hr class="w-100" />
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="container">
            <div class="row justify-content-between">
                <div class="col-7">
                    <div class="row">
                        <!-- LIST OF RANDOM RECIPES -->
                        <div
                            class="col-6 my-2 px-3"
                            v-for="(recipe, index) in randomRecipesArray"
                            :key="`random-recipe-${index}`"
                        >
                            <Card
                                class="text-center box-shadow white mb-4"
                                :card_image="recipe.card_image"
                                :card_title="recipe.card_title"
                                :card_author="recipe.card_author"
                                :card_date="recipe.card_date"
                            />
                        </div>
                    </div>
                </div>
                <div class="col-4">
                    <!-- SEARCH SIDEBAR -->
                    <div class="row pb-5">
                        <div class="col-12">
                            <div class="d-flex">
                                <div class="search_icon cursor-pointer">
                                    <i class="fas fa-search"></i>
                                </div>
                                <input
                                    class="form-control searchbar w-100"
                                    placeholder="Search..."
                                    type="search"
                                />
                            </div>
                        </div>
                    </div>
                    <!-- FOLLOW US SECTION WITH SOCIAL ICONS -->
                    <div class="pb-4">
                        <div class="d-flex fs-5 title-font primary">
                            Follow Us
                        </div>
                    </div>
                    <div class="social-wrapper pb-5">
                        <div class="d-flex pb-3">
                            <i
                                v-for="(social, index) in socialCubesArray"
                                :key="`social-cube-${index}`"
                                class="social-icon text-glow d-flex align-items-center justify-content-center mx-1 cursor-pointer"
                                :class="social.icon"
                            >
                            </i>
                        </div>
                    </div>

                    <PostsWidget />

                    <TweetsWidget />
                </div>

                <!-- LOAD MORE BUTTON -->
                <div class="col-7 pb-7rem">
                    <div
                        class="load-button text-center letter-spacing fs-6 fw-bold py-3 box-shadow cursor-pointer"
                    >
                        LOAD MORE POSTS
                    </div>
                </div>
            </div>
        </div>

        <section>
            <EbookSubscribe />
        </section>

        <section>
            <FullWidthRecipes />
        </section>
    </main>
</template>

<script>
import FoodieJournal from "./FoodieJournal.vue";
import Card from "./Card.vue";
import SectionDivider from "./SectionDivider.vue";
import HoverLink from "./HoverLink.vue";
import PopularRecipes from "./PopularRecipes.vue";
import CulinaryCollections from "./CulinaryCollections.vue";
import PostsWidget from "./PostsWidget.vue";
import TweetsWidget from "./TweetsWidget.vue";
import EbookSubscribe from "./EbookSubscribe.vue";
import FullWidthRecipes from "./FullWidthRecipes.vue";

export default {
    name: "Main",
    components: {
        FoodieJournal,
        Card,
        SectionDivider,
        HoverLink,
        PopularRecipes,
        CulinaryCollections,
        PostsWidget,
        TweetsWidget,
        EbookSubscribe,
        FullWidthRecipes,
    },

    data() {
        return {
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
            randomRecipesArray: [
                {
                    card_image: "fi-roundup-400x263.jpg",
                    card_title:
                        "Roundup: My New Favourite Recipes For Healty Living",
                    card_author: "admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-korean-food-400x263.jpg",
                    card_title: "Meal Prep: Korean Bibimbap with Kimchi",
                    card_author: "admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-toasts-400x263.jpg",
                    card_title: "Why These Toasts with Tea are My New Favorite",
                    card_author: "admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-street-food-400x263.jpg",
                    card_title: "Exploring Street Food in Bangkok",
                    card_author: "admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-organic-breakfast-400x263.jpg",
                    card_title: "Organic Choices For Healthier Living",
                    card_author: "admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-water-side-rest-400x263.jpg",
                    card_title:
                        "5 Waterside Restaurants in Istanbul for Special Events",
                    card_author: "admin",
                    card_date: "March 25th, 2019",
                },
            ],
            socialCubesArray: [
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

.container.white {
    box-shadow: 0px 0px 7px 0px #0000002e, 0px 0px 0px 0px rgb(0 0 0 / 0%);
    padding: 2rem 2rem;
    top: -70px;
}

.latest-recipes-banner {
    background-image: url(/img/ad-bg.e0bca1ff.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    height: 480px;
    background-position: right;
}

.singapore-guide {
    background-image: url(../assets/singapore-featured-image-400x263.jpg);
    background-size: cover;
    height: 264px;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    padding-bottom: 3rem;
    color: white;
    .guide-text {
        background-color: rgba(0, 0, 0, 0.705);
        height: 50px;
        width: 75%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: Catamaran, Arial, Helvetica, sans-serif;
    }
}

.searchbar {
    border-left: 2px solid transparent;
    border-bottom: 1px solid #e2e2e2;
    border-right: 1px solid #e2e2e2;
    border-top: 1px solid #e2e2e2;
    border-top-right-radius: 5px;
    border-bottom-right-radius: 5px;
    height: 60px;
    padding: 5px;
}

.search_icon {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 60px;
    width: 95px;
    color: #d4d6d7;
    background-color: white;
    border-left: 1px solid #e2e2e2;
    border-right: 1px solid transparent;
    border-bottom: 1px solid #e2e2e2;
    border-top: 1px solid #e2e2e2;
    border-top-left-radius: 5px;
    border-bottom-left-radius: 5px;
}

.social-icon {
    color: $small-text-color;
    background-color: #edede8;
    height: 35px;
    width: 35px;
    border-radius: 5px;
    border: 0.5px solid rgb(230, 230, 230);
}

.load-button {
    background-color: #efefe9;
    transition: background 0.4s ease-in-out;
    &:hover {
        background-color: #d6d6d6;
    }
}
</style>
