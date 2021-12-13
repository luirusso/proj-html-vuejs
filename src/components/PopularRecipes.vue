<template>
    <div>
        <div class="row justify-content-between">
            <div class="col-6 big_card white h-75 width-45 p-0 pb-4 box-shadow">
                <div class="w-100 position-relative">
                    <HoverLink
                        :linkTitle="`Lunch Favourite with Salad, Naan And Beans`"
                    />
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
                        Suspendisse at semper odio. Nam fringilla scelerisque
                        tincidunt. Orci varius natoque penatibus et magnis dis
                        parturient montes, nascetur ridiculus mus. Donec
                        tincidunt posuere ornare. Phasellus placerat odio non
                        feugiat sollicitudin. Integer vitae elementum ex. Sed
                        porttitor, diam eget convallis volutpat, arcu tellus
                        facilis nulla, id dignissim orci leo id.
                    </p>
                    <span
                        class="button_site_square small-border py-2 px-3 fw-bold"
                        >LEARN MORE</span
                    >
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
                            <div class="position-relative">
                                <HoverLink :linkTitle="popular.popularTitle" />
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
</template>

<script>
import HoverLink from "./HoverLink.vue";

export default {
    name: "PopularRecipes",
    components: {
        HoverLink,
    },
    data() {
        return {
            popularFoodArray: [
                {
                    popularImage: "Mixed-fruits-400x263.jpg",
                    popularTitle:
                        "Fruit Platter with Banana, Mango, Berries and Orange",
                },
                {
                    popularImage:
                        "r-rachel-park-366508-unsplash-min-400x263.jpg",
                    popularTitle:
                        "Breakfast Delight with Strawberry, Egg and Fruit",
                },
                {
                    popularImage:
                        "r-michelle-tsang-500721-unsplash-min-400x263.jpg",
                    popularTitle:
                        "Ice Cream Heaven with Vanilla, Chocolate and Pistachio",
                },
                {
                    popularImage: "quick-summer-drink-460x295.jpg",
                    popularTitle:
                        "Video Recipe: How To Make a Cool Summer Drink",
                },
                {
                    popularImage:
                        "r-maarten-van-den-heuvel-400626-unsplash-min-460x295.jpg",
                    popularTitle:
                        "Ketogenic Diet Recipe with Avocado",
                },
                {
                    popularImage: "perfect-cosmopolitan-460x295.jpg",
                    popularTitle:
                        "Video Recipe: The Perfect Cosmopolitan",
                },
                {
                    popularImage: "fi2x-6-460x295.jpg",
                    popularTitle:
                        "Summer Cheese Platter with berries, Crackers and Wine",
                },
                {
                    popularImage:
                        "r-brooke-lark-96398-unsplash-min-460x295.jpg",
                    popularTitle:
                        "Strawberry Fruit Pies Served with Tea",
                },
            ],
        };
    },
};
</script>

<style scoped lang="scss">
.popular-food-card {
    max-height: 177px;
    img {
        object-fit: cover;
        width: 100%;
    }
}
</style>
