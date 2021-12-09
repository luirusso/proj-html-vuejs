<template>
    <div
        class="jumbotron d-flex flex-column align-content-center justify-content-center"
    >
        <div class="container_small text-center d-flex flex-column">
            <div>
                <div class="jumbo-title fs-1 position-relative">
                    <div>
                        <span class="today button_site fs-6 fw-bold position-absolute">
                            TODAY'S PICK
                        </span>
                    </div>
                    <div class="jumbo-main-title pb-1">
                        Food Corner: Top Japanese Restaurants for Sushi
                    </div>
                    <div class="fs-5">March 25, 2019</div>
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
    padding: 3rem 4rem;
    -webkit-box-shadow: 0px 10px 13px -7px #000000,
        5px 5px 15px 5px rgba(0, 0, 0, 0);
    box-shadow: 0px 10px 13px -7px #000000, 5px 5px 15px 5px rgba(0, 0, 0, 0);
}

.jumbo-main-title {
    font-family: 'Vidaloka', serif;
}

.button_site {
    top: -10%;
    left: 50%;
    transform: translate(-50%);
    border-radius: 10px;
    padding: 8px 20px;
}

.today {
    box-shadow: 0px 0px 7px 0px #4e4e4e, 0px 0px 0px 0px rgb(0 0 0 / 0%);
}
</style>
