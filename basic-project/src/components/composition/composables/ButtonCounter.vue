<template>
    <div>
        <button @click="incrementCount">Clicked {{ count }} times</button>

    </div>
</template>

<script>
import useCounter from '@/composables/useCounter'


export default {
    name: 'ButtonCounter',
    setup() {
        const {count, incrementCount} = useCounter(100, 2);
        return {count, incrementCount};
    }
}
</script>

<style scoped>
</style>