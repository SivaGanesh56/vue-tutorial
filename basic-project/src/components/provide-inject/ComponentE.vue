<template>
    <div>
        <h3>Component E</h3>
        <ComponentF />
    </div>
</template>

<script>
    import ComponentF from './ComponentF.vue'
    export default {
         name: 'ComponentE',
         components: {
            ComponentF,
         }
    }
</script>

<style scoped>

</style>