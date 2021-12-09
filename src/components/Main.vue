<template>
    <main>
        <div class="container position-relative">
            <div
                class="d-flex pb-4 justify-content-space-between align-items-center"
            >
                <hr />
                <div class="title_spacing flex-grow-1 text-center">
                    <div class="fs-4">FOODIE JOURNAL</div>
                </div>
                <hr />
            </div>
            <div class="site_card d-flex text-center">
                <!-- CARD -->
                <div>
                    <div class="pb-3">
                        <img
                            src="../assets/single-post-img3-400x263.jpg"
                            alt=""
                        />
                    </div>
                    <div class="fs-4">
                        Food Corner: Top Japanese Restaurants for Sushi
                    </div>
                    <div class="d-flex justify-content-center">
                        <div>By admin</div>
                        <div>|</div>
                        <div>March 25th, 2019</div>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
export default {
    name: "Main",
    data() {
        return {
            foodieJournalArray: [
                {
                    card_image: "single-post-img3-400x263.jpg",
                    card_title: "Food Corner: Top Japanese Restaurants for Sushi",
                    card_author: "By admin",
                    card_date: "March 25th, 2019",
                },
                {
                    card_image: "fi-roundup-400x263.jpg",
                    card_title: "Roundup: My New Favourite Recipes For Healthy Living",
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

.container {
    background-color: white;
    box-shadow: 0px 0px 7px 0px #4e4e4e, 0px 0px 0px 0px rgb(0 0 0 / 0%);
    padding: 2rem 3rem;
    top: -70px;
}

.site_card {
    width: calc(100% / 3);
}
</style>
