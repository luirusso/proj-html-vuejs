<template>
    <div class="background d-flex align-items-center justify-content-center box-shadow">
        <div>
            <div class="text-center">
                <div class="pb-3 title-font">
                    <h2>Subscribe <span class="primary">&</span> Receive a Free eBook</h2>
                </div>
                <div>
                    Aliquam erat volutpat. Ut quis ligula a magna blandit
                    finibus. Suspendisse maximus lacus non nunc lacinia
                    lobortis.
                </div>
            </div>
            <div class="text-center d-flex justify-content-center py-5">
                <input
                    class="form-control ebook w-50 me-4"
                    placeholder="Insert your email... *"
                    type="email"
                />
                <button class="button_site_square fs-5">SUBSCRIBE</button>
            </div>
            <div class="text-center">
                Cras porttitor pellentesque sem eu pretium.
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "EbookSubscribe",
};
</script>

<style scoped lang="scss">
@import "../styles/globals.scss";

.background {
    background-image: url(../assets/subscribe-sec-bg.png);
    background-size: cover;
    height: 550px;
}

.button_site_square {
    border: none;
    padding: 12px 50px;
    border-radius: 5px;
}

.ebook {
    padding: 13px 50px;
    border-radius: 5px;
    border: 2px solid lightgray;
    &:hover {
        border: 2px solid rgba(255, 68, 0, 0.322);
    }
    &:focus {
        border: 2px solid $primary-color;
        box-shadow: none;
    }
}
</style>
