<template>
    <div>
        <input type="text" v-model="first" />
        <input type="text" v-model="last" />
        <h3>FullName: {{ fullName }}</h3>

        <input type="text" v-model="refFirst" />
        <input type="text" v-model="refLast" />
        <h3>Ref FullName: {{ refFullName }}</h3>

        <input type="text" v-model="reactiveFirst" />
        <input type="text" v-model="reactiveLast" />
        <h3>Reactive FullName: {{ reactiveFullName }}</h3>

    </div>
</template>

<script>
import { ref, computed, reactive, toRefs } from '@vue/reactivity';
    export default {
        name: 'Computed',
        setup() {
            const refFirst = ref('');
            const refLast = ref('');

            const refFullName = computed(function() {
                return `${refFirst.value} ${refLast.value}`;
            });

            const state = reactive({
                reactiveFirst: '',
                reactiveLast: ''
            });

            const reactiveFullName = computed(function() {
                return `${state.reactiveFirst} ${state.reactiveLast}`;
            });

            return {
                refFirst,
                refLast,
                refFullName,
                ...toRefs(state),
                reactiveFullName,
            };
        },
        data() {
            return {
                first: '',
                last: ''
            }
        },
        computed: {
            fullName() {
                return this.first + ' ' +  this.last;
            }
        }
    }
</script>

<style scoped>

</style>