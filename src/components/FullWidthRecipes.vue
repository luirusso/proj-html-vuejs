<template>
    <div>
        <div class="row p-0 m-0">
            <div v-for="(recipe, index) in recipes" :key="`recipe-${index}`" class="col-3 p-0 m-0 position-relative">
                <HoverLink 
                :linkTitle="recipe.title"
                />
                <img
                    class="w-100"
                    :src="require(`../assets/${recipe.image}`)"
                    alt=""
                />
            </div>
        </div>
    </div>
</template>

<script>
import HoverLink from "./HoverLink.vue";

export default {
    name: "FullWidthRecipes",
    components: {
        HoverLink,
    },
    data () {
        return {
            recipes: [
                {
                    image: 'Yogurt-Nan-600x395.jpg',
                    title: 'Lunch Favourite with Salad, Naan and Beans',
                },
                {
                    image: 'Mixed-fruits-600x395.jpg',
                    title: 'Fruit Platter with Banana, Mango, Berries and Orange',
                },
                {
                    image: 'r-rachel-park-366508-unsplash-min-600x395.jpg',
                    title: 'Breakfast Delight with Strawberry, Egg and Fruit',
                },
                {
                    image: 'r-michelle-tsang-500721-unsplash-min-600x395.jpg',
                    title: 'Ice Cream Heaven with Vanilla, Chocolate and Pistachio',
                },
            ]
        }
    },
};
</script>

<style scoped lang="scss"></style>
