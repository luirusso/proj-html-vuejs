<template>
    <div class="col-12">
        <div class="tweets-wrapper p-4">
            <div class="d-flex justify-content-between pb-4">
                <div>
                    <span>Tweets </span> <span>by</span>
                    <span>@Theme_Fusion</span>
                </div>
                <div>
                    <img src="../assets/image.svg" alt="" />
                </div>
            </div>
            <div class="d-flex justify-content-between">
                <div class="d-flex align-items-center">
                    <img class="pe-2"
                        src="../assets/3a74ce3d0532b7773b174c45ca3bd05a_normal.png"
                        alt=""
                    />
                    <div class="d-flex flex-column">
                        <span>ThemeFusion</span> <span>@Theme_Fusion</span>
                    </div>
                </div>
                <div>
                    <img class="twitter-icon" src="../assets/image (1).svg" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "TweetsWidget",
};
</script>

<style scoped lang="scss">
.tweets-wrapper {
    background-color: white;
    border-radius: 10px;
}

.twitter-icon {
    width: 25px;
}
</style>
