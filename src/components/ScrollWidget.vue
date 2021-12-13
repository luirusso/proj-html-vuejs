<template>
    <a
        class="scroll-icon d-flex align-items-center justify-content-center position-fixed"
        href="#header"
        ><i class="fas fa-angle-up"></i
    ></a>
</template>

<script>
export default {
    name: "ScrollWidget",
};
</script>

<style scoped lang="scss">
a {
    color: unset;
    &:hover {
        color: unset;
    }
}

.scroll-icon {
    z-index: 1;
    height: 45px;
    width: 45px;
    border-radius: 50%;
    background-color: #464646bb;
    color: white;
    bottom: 3%;
    left: 4%;
    transition: all 0.4s ease-in-out;
    &:hover {
        cursor: pointer;
        background-color: #fc7a23;
        color: white;
        box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
        cursor: pointer;
    }
}
</style>
