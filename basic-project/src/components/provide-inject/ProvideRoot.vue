<template>
    <div>

        <h3>Name - {{ name }}</h3>

        <h3>Full Name - {{ first }} {{ last }}</h3>

        <h3>Count - {{ count }}</h3>

        <button @click="incrementCount">Increment</button>
        <ComponentC />
    </div>
</template>

<script>
import { provide, reactive, ref, toRefs } from 'vue';
import ComponentC from './ComponentC.vue'
export default {
    name: "ProvideVue",
    components: {
        ComponentC
    },
    setup() {
        provide('c_username', 'Siva Ganesh');

        const name = ref('Siva');
        const state = reactive({
            first: 'Siva',
            last: 'Ganesh'
        });


        provide('c_name', name);
        provide('c_state', state);

        const count = ref(0);
        
        function incrementCount() {
            count.value++;
        }

        provide('c_count', count);
        provide('c_increment', incrementCount);


        return {
            name,
            ...toRefs(state),
            count,
            incrementCount,
        }
    },
    provide() {
        return {
            username: this.name
        }
    }
}
</script>

<style scoped>
</style>