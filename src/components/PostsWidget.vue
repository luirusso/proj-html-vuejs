<template>
    <div class="d-flex align-items-center pb-5">
        <div class="pe-3">
            <img
                class="round cursor-pointer"
                :src="require(`../assets/${image}`)"
                :alt="title"
            />
        </div>
        <div>
            <div class="fs-6 cursor-pointer text-glow">
                {{title}}
            </div>
            <div class="date">{{date}}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'PostsWidget',
    props: {
        image: String,
        title: String,
        date: String,
    }
};
</script>

<style scoped lang="scss">
@import "../styles/globals.scss";
.date {
    color: $small-text-color;
}

img {
    max-width: 55px;
}
</style>
