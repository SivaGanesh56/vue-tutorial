<template>
    <div>
        <!-- <button @click="getPosts">Load Posts</button> -->

        <h3 v-show="errMessage">{{ errMessage }}</h3>

        <div v-for="post of posts" :key="post.id">
            <h3>{{ post.id }} {{ post.title }}</h3>
            <p>{{ post.body }}</p>
            <hr />
        </div>
    </div>
</template>

<script>
    import axios from 'axios';
    export default {
        name: 'PostList',
        created() {
            this.getPosts();
        },
        data() {
            return {
                posts: [],
                errMessage: ''
            }
        },
        methods: {
            getPosts: async function() {
                try {
                    const { data } = await axios.get('https://jsonplaceholder.typicode.com/posts');
                    this.posts = data;
                } catch (error) {
                    console.log('Error while reterving the data');
                    this.errMessage = 'Error occured!'
                }
            }
        }
    }
</script>

<style scoped>

</style>