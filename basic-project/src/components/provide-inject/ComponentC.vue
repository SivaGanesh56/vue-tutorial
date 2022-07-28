<template>
    <div>
        <h3>Component C</h3>
        <ComponentE />
    </div>
</template>

<script>
    import ComponentE from './ComponentE.vue'
    export default {
        name: 'ComponentC',
        components: {
            ComponentE
        }
    }
</script>

<style scoped>

</style>