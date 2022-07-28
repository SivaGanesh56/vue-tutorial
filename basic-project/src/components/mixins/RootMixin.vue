<template>
    <div>
        <ButtonCounter />
        <HoverCounter />
    </div>
</template>

<script>
import ButtonCounter from './ButtonCounter.vue';
import HoverCounter from './HoverCounter.vue';
    export default {
    name: "RootMixin",
    components: { ButtonCounter, HoverCounter }
}
</script>

<style scoped>

</style>