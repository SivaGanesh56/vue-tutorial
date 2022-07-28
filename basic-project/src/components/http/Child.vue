<template>
    <div>
        <h3>Child Component</h3>
    </div>
</template>

<script>
    export default {
        name: 'Child',
        beforeCreated() {
            console.log('Child before created')
        },
        created() {
            console.log('Child Created');
        },
        beforeMount() {
            console.log('Child before mount');
        },
        mounted() {
            console.log('Child mounted');
        },
        beforeUpdate() {
            console.log('Child before updated');
        },
        updated() {
            console.log('Child updated');
        },
        beforeUnmount() {
            console.log('Child before unmount');
        },
        unmounted() {
            console.log('Child unmounted');
        }
    }
</script>

<style scoped>

</style>