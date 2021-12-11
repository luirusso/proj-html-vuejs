<template>
    <div class="width-100">
        <div class="width-100 mb-3 position-relative">
            <HoverLink />
            <img
                class="width-100"
                :src="require(`../assets/${card_image}`)"
                alt=""
            />
        </div>
        <div class="px-4 pb-4">
            <div class="title-font text-glow fs-4 pb-1">{{ card_title }}</div>
            <div class="d-flex justify-content-center">
                <div>{{ card_author }}</div>
                <div class="px-1">|</div>
                <div>{{ card_date }}</div>
            </div>
        </div>
    </div>
</template>

<script>
import HoverLink from "./HoverLink.vue";

export default {
    name: "Card",
    components: {
        HoverLink,
    },
    props: {
        card_image: String,
        card_title: String,
        card_author: String,
        card_date: String,
    },
};
</script>

<style scoped lang="scss"></style>
