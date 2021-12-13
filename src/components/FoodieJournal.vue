<template>
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
        <div class="row d-flex text-center justify-content-center">
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
</template>

<script>
import Card from "./Card.vue";

export default {
    name: "FoodieJournal",
    components: {
        Card,
    },

    data() {
        return {
            foodieJournalArray: [
                {
                    card_image: "single-post-img3-400x263.jpg",
                    card_title:
                        "Food Corner: Top Japanese Restaurants for Sushi",
                    card_author: "admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-roundup-400x263.jpg",
                    card_title:
                        "Roundup: My New Favourite Recipes For Healthy Living",
                    card_author: "admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-toasts-400x263.jpg",
                    card_title: "Why These Toasts with Tea are My New Favorite",
                    card_author: "admin",
                    card_date: "March 25th, 2019",
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
</style>
