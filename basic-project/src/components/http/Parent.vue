<template>
    <div>
        <h3>Parent Component</h3>
        <button @click="show = !show">Toggle Child</button>
        <Child v-if="show" />
    </div>
</template>

<script>
import Child from './Child.vue';
export default {
    name: "Parent",
    data() {
        return {
            show: true,
        };
    },
    beforeCreated() {
        console.log("Parent before created");
    },
    created() {
        console.log("Parent Created");
    },
    beforeMount() {
        console.log("Parent before mount");
    },
    mounted() {
        console.log("Parent mounted");
    },
    beforeUpdate() {
        console.log("Parent before updated");
    },
    updated() {
        console.log("Parent updated");
    },
    beforeUnmount() {
        console.log("Parent before unmount");
    },
    unmounted() {
        console.log("Parent unmounted");
    },
    components: { Child }
}
</script>

<style scoped>
</style>