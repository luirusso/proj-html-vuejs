<template>
    <main>
        <div class="container white pb-4 position-relative">
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
                    class="card-site col-4 px-4"
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
                class="text-center"
                :title="`POPULAR RECIPES`"
                :text="`Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.`"
            />
        </div>

        <div class="container pb-5">
            <div class="row justify-content-between">
                <div
                    class="col-6 big_card white h-75 width-45 p-0 pb-4 box-shadow"
                >
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
                            <h4 class="title-font text-glow">
                                Lunch Favourite with Salad, Naan And Beans
                            </h4>
                            <div class="pb-1">
                                Bakery, Featured, Healthy, Latest Recipes, Staff
                                Picks
                            </div>
                        </div>
                        <div class="pb-1">
                            <hr class="w-100 my-3" />
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
                        <span class="button_site_square">LEARN MORE</span>
                    </div>
                </div>
                <div class="col-6">
                    <div class="row">
                        <div
                            v-for="(popular, index) in popularFoodArray"
                            :key="`popular-${index}`"
                            class="col-6 pb-3 pe-2"
                        >
                            <!-- POPULAR FOOD CARDS -->
                            <div
                                class="popular-food-card overflow-hidden w-100 box-shadow"
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
                    <div class="button_site_square">
                        READ OUR BLOG
                        <span><i class="fas fa-book-reader"></i></span>
                    </div>
                </div>
            </div>
        </div>

        <div class="container">
            <div class="row justify-content-between">
                <div class="col-7">
                    <div class="big_card white p-0 pb-4 mb-5 box-shadow">
                        <div class="w-100 position-relative">
                            <HoverLink />
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
                    <div class="row pb-5">
                        <div class="col-12">
                            <div class="d-flex">
                                <div class="search_icon">
                                    <i class="fas fa-search"></i>
                                </div>
                                <input
                                    class="searchbar w-100"
                                    placeholder="Search..."
                                    type="search"
                                />
                            </div>
                        </div>
                    </div>
                    <div class="pb-4">
                        <div class="d-flex fs-5 title-font primary">
                            Follow Us
                        </div>
                    </div>
                    <div class="social-wrapper pb-5">
                        <div class="d-flex">
                            <i
                                v-for="(social, index) in socialCubesArray"
                                :key="`social-cube-${index}`"
                                class="social-icon d-flex align-items-center justify-content-center mx-1 cursor-pointer"
                                :class="social.icon"
                            >
                            </i>
                        </div>
                    </div>
                    <div class="col-12 pb-5">
                        <div class="row">
                            <div
                                class="col-6 side-post-title text-center title-font white d-flex align-items-center justify-content-center cursor-pointer text-glow"
                            >
                                Popular
                            </div>
                            <div
                                class="col-6 side-post-title text-center title-font d-flex align-items-center justify-content-center cursor-pointer text-glow"
                            >
                                Recent
                            </div>
                        </div>
                    </div>
                    <div class="pb-5">
                        <div
                            v-for="(post, index) in postsWidgetArray"
                            :key="`post-${index}`"
                            class="col-12"
                        >
                            <PostsWidget
                                :image="post.image"
                                :title="post.title"
                                :date="post.date"
                            />
                        </div>
                    </div>

                    <TweetsWidget />
                </div>

                <div class="col-7 pb-7rem">
                    <div class="load-button text-center fs-5 fw-bold py-3 box-shadow cursor-pointer">
                        LOAD MORE POSTS
                    </div>
                </div>
            </div>
        </div>

        <section>
            <EbookSubscribe />
        </section>

        <section class="pb-5">
            <div class="row p-0 m-0">
                <div class="col-3 p-0 m-0 position-relative">
                    <HoverLink />
                    <img class="w-100" src="../assets/Yogurt-Nan-600x395.jpg" alt="">
                </div>
                <div class="col-3 p-0 m-0 position-relative">
                    <HoverLink />
                    <img class="w-100" src="../assets/Mixed-fruits-600x395.jpg" alt="">
                </div>
                <div class="col-3 p-0 m-0 position-relative">
                    <HoverLink />
                    <img class="w-100" src="../assets/r-rachel-park-366508-unsplash-min-600x395.jpg" alt="">
                </div>
                <div class="col-3 p-0 m-0 position-relative">
                    <HoverLink />
                    <img class="w-100" src="../assets/r-michelle-tsang-500721-unsplash-min-600x395.jpg" alt="">
                </div>
            </div>
        </section>
    </main>
</template>

<script>
import Card from "./Card.vue";
import SectionDivider from "./SectionDivider.vue";
import HoverLink from "./HoverLink.vue";
import CulinaryCollections from "./CulinaryCollections.vue";
import PostsWidget from "./PostsWidget.vue";
import TweetsWidget from "./TweetsWidget.vue";
import EbookSubscribe from "./EbookSubscribe.vue";

export default {
    name: "Main",
    components: {
        Card,
        SectionDivider,
        HoverLink,
        CulinaryCollections,
        PostsWidget,
        TweetsWidget,
        EbookSubscribe,
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
            randomRecipesArray: [
                {
                    card_image: "fi-roundup-400x263.jpg",
                    card_title:
                        "Roundup: My New Favourite Recipes For Healty Living",
                    card_author: "By admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-korean-food-400x263.jpg",
                    card_title: "Meal Prep: Korean Bibimbap with Kimchi",
                    card_author: "By admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-toasts-400x263.jpg",
                    card_title: "Why These Toasts with Tea are My New Favorite",
                    card_author: "By admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-street-food-400x263.jpg",
                    card_title: "Exploring Street Food in Bangkok",
                    card_author: "By admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-organic-breakfast-400x263.jpg",
                    card_title: "Organic Choices For Healthier Living",
                    card_author: "By admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-water-side-rest-400x263.jpg",
                    card_title:
                        "5 Waterside Restaurants in Istanbul for Special Events",
                    card_author: "By admin",
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
            postsWidgetArray: [
                {
                    image: "single-post-img3-66x66.jpg",
                    title: "Food Corner: Top Japanes Restaurants for Sushi",
                    date: "March 25th, 2019",
                },
                {
                    image: "singapore-featured-image-66x66.jpg",
                    title: "City Guide: Singapore",
                    date: "February 27th, 2019",
                },
                {
                    image: "slide1-bg-66x66.jpg",
                    title: "6 Nutritional Tips to Help Burn Down Body Fat",
                    date: "February 28th, 2019",
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
    border: none;
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
    border-bottom: 1px solid #e2e2e2;
    border-top: 1px solid #e2e2e2;
    border-top-left-radius: 5px;
    border-bottom-left-radius: 5px;
}

.social-icon {
    background-color: #edede8;
    height: 35px;
    width: 35px;
    border-radius: 5px;
    border: 0.5px solid grey;
}

.side-post-title {
    height: 50px;
    border: 0.5px solid lightgray;
}

.load-button {
    background-color: #EFEFE9;
    transition: background 0.4s ease-in-out;
    &:hover {
        background-color: #d6d6d6;
    }
}
</style>
