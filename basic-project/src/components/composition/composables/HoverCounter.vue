<template>
    <div>
        <button @mouseover="incrementCount">Hovered {{ count }} times</button>
    </div>
</template>

<script>
import useCounter from '@/composables/useCounter'


export default {
    name: 'HoverCounter',
    setup() {
        const { count, incrementCount } = useCounter();

        return { count, incrementCount }
    }
}
</script>

<style scoped>
</style>