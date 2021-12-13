<template>
    <div
        class="hover-link title-font fs-5 d-flex flex-column align-content-center justify-content-center text-center px-5"
    >
        <div class="d-flex flex-column align-items-center justify-content-center pb-2">
            <div
                class="link-icon d-flex align-items-center justify-content-center mb-2"
            >
                <i class="fas fs-6 fa-link"></i>
            </div>
            <div class="white-text">{{ linkTitle }}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: "HoverLink",
    props: {
        linkTitle: String,
    },
};
</script>

<style scoped lang="scss">
.white-text {
    color: white;
}

.hover-link {
    height: 100%;
    width: 100%;
    background: linear-gradient(
        180deg,
        rgba(251, 78, 35, 0.616) 0%,
        rgba(251, 96, 35, 1) 100%
    );
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
