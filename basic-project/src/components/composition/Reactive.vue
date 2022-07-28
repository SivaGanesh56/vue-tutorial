<template>
    <div>
        <h3>Reactve - {{ state.first }} {{ state.last }}</h3>
        <input type="number" v-model="state.score"/>
    </div>
</template>

<script>
import { reactive } from '@vue/reactivity'
    export default {
        name: 'Reactive',
        setup() {
            const state = reactive({
                first: 'Siva',
                last: 'Ganesh',
                score: 0,
            });

            return {state};
        }
    }
</script>

<style scoped>

</style>