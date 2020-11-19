<template>
    <div class="recipe">
        <div class ="recipe_title">
            <b>Title: </b> {{title}} <br>
        </div>
        <div class = "recipe_image">
            <img :src="recipimg" >
        </div>
        <div class = "recipe_list">
            <b>Ingredients: </b>
            <ul>
                {{ingredients}}
            </ul>
        </div>
        <div class="recipe_link">
            <b>Link: </b>
            <a :href="link"></a>
        </div>

    </div>
</template>

<script>
    export default {
        name: 'recipListComponent',
        props: ['title','recipimg','ingredients','link']
    }
</script>

<style lang="scss" scoped>

</style>