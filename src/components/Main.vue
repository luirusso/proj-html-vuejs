<template>
    <main>
        <div class="container pb-5 position-relative">
            <div
                class="d-flex pb-4 justify-content-space-between align-items-center"
            >
                <hr />
                <div class="title_spacing flex-grow-1 text-center">
                    <div class="fs-4">FOODIE JOURNAL</div>
                </div>
                <hr />
            </div>
            <div class="row site_card d-flex text-center justify-content-center">
                <!-- CARD -->
                <div class="card-site col-4"
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
    </main>
</template>

<script>
import Card from "./Card.vue";

export default {
    name: "Main",
    components: {
      Card
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

.container {
    background-color: white;
    box-shadow: 0px 0px 7px 0px #4e4e4e, 0px 0px 0px 0px rgb(0 0 0 / 0%);
    padding: 2rem 3rem;
    top: -70px;
}

</style>
