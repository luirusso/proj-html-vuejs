<template>
    <div class="width-100 px-2">
        <div class="width-100 pb-3">
            <img class="width-100" :src="require(`../assets/${card_image}`)" alt="" />
        </div>
        <div class="title-font fs-4 pb-1">{{ card_title }}</div>
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
