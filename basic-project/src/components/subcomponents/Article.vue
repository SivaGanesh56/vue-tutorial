<template>
    <div>
        <h3>Title - {{ title }}</h3>

        <h3 v-bind="$attrs">Publish Status - {{ published ? "YES": "NO" }}</h3>

        <h3>No of Comments - {{ noOfComments }}</h3>

    </div>
</template>

<script>
    export default {
        name: 'ArticleVue',
        props: {
            title: {
                type: String,
                required: true,
                default: 'Default Title'
            },
            published: Boolean,
            noOfComments: Number,
        },
        inheritAttrs: false
    }
</script>

<style scoped>

</style>