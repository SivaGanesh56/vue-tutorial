<template>
    <div>
        <button @mouseover="increment">Hovered {{ count }} times</button>
    </div>
</template>

<script>
import counter from '@/mixins/counter';

export default {
    name: 'HoverCounter',
    mixins: [counter]
}
</script>

<style scoped>
</style>