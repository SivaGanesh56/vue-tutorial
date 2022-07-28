<template>
    <div>
        <h3>Name - {{ name }}</h3>
        <button @click="changeName">Change Name</button>

        <h3>Ref Count - {{ count }}</h3>
        <button @click="increment">Increment</button>

        <h3>Reactive - {{ first }} {{ last }}</h3>
        <button @click="changeNames">Change Names</button>
    </div>
</template>

<script>
import { reactive, ref, toRefs } from '@vue/reactivity'
    export default {
        name: 'Methods',
        setup() {
            const count = ref(0);

            function increment() {
                count.value+=1;
            }

            const state = reactive({
                first: 'Siva',
                last: 'Ganesh'
            });

            function changeNames() {
                state.first = 'MS';
                state.last = 'Dhoni';
            }

            return {
                count,
                increment,
                ...toRefs(state),
                changeNames,
            };
        },
        data() {
            return {
                name: 'Siva'
            }
        },
        methods: {
            changeName() {
                this.name = 'Ganesh'
            }
        }
    }
</script>

<style scoped>

</style>