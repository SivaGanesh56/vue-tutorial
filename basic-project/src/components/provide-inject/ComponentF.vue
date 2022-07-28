<template>
    <div>
        <h3>Component F - {{ username }}</h3>

        <h3>Inject username - {{ c_username }}</h3>

        <h3>Inject c_name - {{ c_name }}</h3>

        <h3>Inject Full Name - {{ first }} {{ last }}</h3>

        <h3>Injected Count - {{ count }}</h3>

        <button @click="incrementCount">Increment</button>
    </div>
</template>

<script>
import { inject, toRefs } from 'vue'

    export default {
         name: 'ComponentF',
         inject: ['username'],
         setup() {
            const c_username = inject('c_username', 'Default UserName');
            const c_name = inject('c_name', 'c_name');
            const state = inject('c_state', {});

            const count = inject('c_count', 0);
            const incrementCount = inject('c_increment');

            return {
                c_username,
                c_name,
                ...toRefs(state),
                count,
                incrementCount
            }
         }
    }
</script>

<style scoped>

</style>