<template>
    <div class="white width-90 box-shadow">
        <div class="p-1">
            <div class="d-flex justify-content-center align-items-center">
                <div class="d-flex justify-content-center py-3">
                    <img :src="require(`../assets/${image}`)" alt="" />
                </div>
            </div>
        </div>
        <div>
            <div class="button_site text-center">{{ button }}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: "CulinaryCollections",
    props: {
        image: String,
        button: String,
    },
};
</script>

<style scoped lang="scss">
img {
    width: 65%;
    transition: transform 0.7s ease-in-out;
    &:hover {
        transform: scale(1.1);
        cursor: pointer;
    }
}
</style>
