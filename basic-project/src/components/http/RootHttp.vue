<template>
    <div>
        <CreatePost />
        <PostList />
        <Parent />
    </div>
</template>

<script>
import PostList from './PostList.vue';
import CreatePost from './CreatePost.vue';
import Parent from './Parent.vue';
    export default {
    name: "RootHttp",
    components: { PostList, CreatePost, Parent }
}
</script>

<style scoped>

</style>