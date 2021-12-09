<template>
    <div class="px-3">
        <div class="pb-3">
            <img :src="require(`../assets/${card_image}`)" alt="" />
        </div>
        <div class="fs-4">{{ card_title }}</div>
        <div class="d-flex justify-content-center">
            <div>{{ card_author }}</div>
            <div class="px-1">|</div>
            <div>{{ card_date }}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Card",
    props: {
        card_image: String,
        card_title: String,
        card_author: String,
        card_date: String,
    },
};
</script>

<style scoped lang="scss">

</style>
