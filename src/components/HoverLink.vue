<template>
    <div class="hover-link d-flex flex-column align-content-center justify-content-center text-center py-4 px-5">
        <div class="d-flex justify-content-center pb-2">
            <div
                class="link-icon d-flex align-items-center justify-content-center"
            >
                <i class="fas fa-link"></i>
            </div>
        </div>
        <div>Fruit Platter with Banana, Mango, Berries and Orange</div>
    </div>
</template>

<script>
export default {
    name: "HoverLink",
};
</script>

<style scoped lang="scss">
.hover-link {
    height: 100%;
    width: 100%;
    background-color: rgba(255, 68, 0, 0.644);
    color: white;
    position: absolute;
    opacity: 0;
    transition: opacity 0.4s ease-in-out;
    &:hover {
        opacity: 1;
        cursor: pointer;
    }
}

.link-icon {
    height: 40px;
    width: 40px;
    background-color: white;
    border-radius: 50%;
    color: rgba(255, 68, 0, 0.644);
}
</style>
