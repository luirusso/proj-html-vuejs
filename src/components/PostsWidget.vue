<template>
    <div class="pb-4">
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
        <div
            v-for="(post, index) in postsWidgetArray"
            :key="`post-${index}`"
            class="col-12"
        >
            <div class="d-flex align-items-center pb-5">
                <div class="pe-3">
                    <img
                        class="round cursor-pointer"
                        :src="require(`../assets/${post.image}`)"
                        :alt="post.title"
                    />
                </div>
                <div>
                    <div class="fs-6 cursor-pointer text-glow">
                        {{ post.title }}
                    </div>
                    <div class="date">{{ post.date }}</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "PostsWidget",
    data() {
        return {
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
.date {
    color: $small-text-color;
}

.side-post-title {
    height: 50px;
    border: 0.5px solid lightgray;
}
img {
    max-width: 55px;
}
</style>
