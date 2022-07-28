<template>
    <div>
        <h3>Greet {{ fullName }}</h3>

        <button @click="sendEvent">Greet Heros</button>
    </div>
</template>

<script>
import { computed } from 'vue'

    export default {
        name: 'PropsGreet',
        setup(props, context) {
            const fullName = computed(() => {
                return `${props.first} ${props.last}`
            });

            function sendEvent() {
                context.emit('call', fullName.value);
            }

            return {
                fullName,
                sendEvent,
            };
        },
        props: ['first', 'last'],
        emits: ['call']
    }
</script>

<style scoped>

</style>