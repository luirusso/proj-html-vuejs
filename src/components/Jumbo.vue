<template>
    <div
        class="jumbotron d-flex flex-column align-content-center justify-content-center"
    >
        <div class="container_small text-center d-flex flex-column">
            <div>
                <div class="jumbo-title box-shadow fs-1 position-relative">
                    <div>
                        <span
                            class="box-shadow today button_site fs-6 fw-bold position-absolute"
                        >
                            TODAY'S PICK
                        </span>
                    </div>
                    <div class="title-font pb-1 text-glow">
                        <h1>Food Corner: Top Japanese Restaurants for Sushi</h1>
                    </div>
                    <div class="fs-5 title-font date">March 25, 2019</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Jumbo",
};
</script>

<style scoped lang="scss">
@import "../styles/globals.scss";

h1 {
    font-size: 45px;
}

.jumbotron {
    height: 700px;
    background-image: url(/img/single-post-img3.80e82235.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position-y: -265px;
}

.jumbo-title {
    background: white;
    border-radius: 10px;
    padding: 2.5rem 4rem;
}

.today {
    letter-spacing: 1px;
}

.date {
    color: $small-text-color;
}

.button_site {
    top: -10%;
    left: 50%;
    transform: translate(-50%);
    border-radius: 10px;
    padding: 8px 30px;
}
</style>
