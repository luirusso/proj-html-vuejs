<template>
    <div class="white width-90 box-shadow">
        <div class="p-1">
            <div class="d-flex justify-content-center align-items-center">
                <div class="d-flex justify-content-center pt-1">
                    <img :src="require(`../assets/${image}`)" alt="" />
                </div>
            </div>
        </div>
        <div class="p-2">
            <div
                class="collection-button text-center d-flex justify-content-center align-items-center"
            >
                {{ button }}
            </div>
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
@import "../styles/globals.scss";
img {
    width: 60%;
    transition: transform 0.7s ease-in-out;
    &:hover {
        transform: scale(1.2);
        cursor: pointer;
    }
}

.collection-button {
    height: 50px;
    width: 100%;
    font-weight: 600;
    transition: background 0.3s ease-in-out, color 0.3s linear;
    &:hover {
        background-color: $primary-color;
        color: white;
        cursor: pointer;
    }
}
</style>
