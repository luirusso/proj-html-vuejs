<template>
    <section class="text-center pb-5">
        <h5 class="pt-5 pb-4 fw-600">{{ title }}</h5>

        <div class="fs-6">
            {{ text }}
        </div>
    </section>
</template>

<script>
export default {
    name: "SectionDivider",
    props: {
        title: String,
        text: String,
    }
};
</script>

<style scoped lang="scss">
h5 {
    letter-spacing: 2px;
}
</style>
