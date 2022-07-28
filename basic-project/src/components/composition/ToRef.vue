<template>
    <div>
        <h3>First Name- {{ first }}</h3>
    </div>
</template>

<script>
import { reactive, toRefs } from '@vue/reactivity'
    export default {
        name: 'ToRef',
        setup() {
            const state = reactive({
                first: 'Siva',
            });

            setTimeout(() => {
                state.first = 'Ganesh'
            }, 2000);

            return toRefs(state);
        }
    }
</script>

<style scoped>

</style>