<template>
    <div>
        <button @click="increment">Clicked {{ count }} times</button>

    </div>
</template>

<script>
import counter from '@/mixins/counter';

export default {
    name: 'ButtonCounter',
    data() {
        return {
            count: 100
        }
    },
    mixins: [counter]
}
</script>

<style scoped>
</style>