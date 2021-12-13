<template>
    <div class="col-12">
        <div class="tweets-wrapper p-4">
            <div class="d-flex justify-content-between pb-4">
                <div>
                    <span class="fs-4">Tweets </span> <span>by </span>
                    <a href="#"><span>@Theme_Fusion</span></a>
                </div>
                <div>
                    <img class="cursor-pointer" src="../assets/image.svg" alt="" />
                </div>
            </div>

            <div class="row">
                <div class="col-2">
                    <div class="d-flex justify-content-between">
                        <div class="d-flex align-items-center">
                            <img
                                class="pe-1 cursor-pointer w-100"
                                src="../assets/3a74ce3d0532b7773b174c45ca3bd05a_normal.png"
                                alt=""
                            />
                        </div>
                    </div>
                </div>
                <div class="col-10">
                    <div class="d-flex justify-content-between">
                        <div class="d-flex flex-column">
                            <span class="fw-bold">ThemeFusion</span>
                            <a href="#"><span class="grey-link">@Theme_Fusion</span></a>
                        </div>
                        <div>
                            <img
                                class="twitter-icon cursor-pointer"
                                src="../assets/image (1).svg"
                                alt=""
                            />
                        </div>
                    </div>
                    <div class="pb-4">
                        Do you need sublime WordPress hosting for your next
                        website? Take advantage of exclusive partner offers that
                        we have secured just for you & launch your site in
                        seconds with
                        <span>#avada</span> on WP Engine hosting & get 30% Off
                        this Black Friday <a href="#">bit.ly/3kjLLE2</a>
                        <span> <a href="#"> #BlackFriday2020</a></span>
                    </div>
                    <div class="pb-2">
                        <img
                            class="post-img-content cursor-pointer w-100"
                            src="../assets/En2TRxLW4AEiWUN.jpeg"
                            alt=""
                        />
                    </div>
                    <div>
                        <div></div>
                        <div class="d-flex justify-content-between">
                            <div class="d-flex">
                                <div class="pe-3">
                                    <img
                                        class="w-75 cursor-pointer"
                                        src="../assets/image (2).svg"
                                        alt=""
                                    />
                                </div>
                                
                                <div>
                                    <img
                                        class="w-75 cursor-pointer"
                                        src="../assets/image (3).svg"
                                        alt=""
                                    />
                                </div>
                            </div>
                            <div>
                                <span class="grey-link">21h</span>
                            </div>
                        </div>
                    </div>
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
@import "../styles/globals.scss";

.tweets-wrapper {
    background-color: white;
    border-radius: 10px;
}

.grey-link {
    color: $primary-text-color;
}

.twitter-icon {
    width: 25px;
}

.post-img-content {
    border-radius: 5px;
}
</style>
