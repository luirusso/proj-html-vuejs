<template>
    <div class="fixed-wrapper position-fixed">
        <div
            class="fixed-icon d-flex flex-column align-items-center justify-content-center mb-2 p-1 cursor-pointer"
        >
            <div class="fixed-animation">
                <i class="fab fs-3 fa-vuejs"></i>
            </div>
            <div>Demos</div>
        </div>
        <div
            class="fixed-icon d-flex flex-column align-items-center justify-content-center p-1 cursor-pointer"
        >
            <div class="fw-bold">
                <div class="green d-flex fixed-animation">
                    <span class="fs-13 pt-2">$</span> <span class="fs-3">39</span>
                </div>
            </div>
            <div>On Sale</div>
        </div>
    </div>
</template>

<script>
export default {
    name: "FixedIcons",
};
</script>

<style scoped lang="scss">
@import "../styles/globals.scss";

.fixed-wrapper {
    right: 0%;
    top: 15%;
    font-family: 'Open Sans', sans-serif;
    z-index: 1;
}

.green {
    color: #65bc7b;
}

.fixed-icon {
    height: 70px;
    width: 70px;
    box-shadow: rgba(0, 0, 0, 0.25) 0px 25px 50px -12px;
    border-radius: 10px;
    background-color: #fdfdfd;
    font-size: 12px;
}

.fixed-animation {
    transition: all 0.4s ease-in-out;
    &:hover {
        transform: rotateZ(360deg);
    }
}
</style>
