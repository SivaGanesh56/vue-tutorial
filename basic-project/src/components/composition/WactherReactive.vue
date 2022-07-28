<template>
    <div>
        <input type="text" label="first Name" v-model="first" />
        <input type="text" label="last Name" v-model="last" />
        <input type="text" label="Role" v-model="options.role" />
    </div>
</template>

<script>
import { reactive, toRefs, watch } from 'vue';
import _ from 'lodash';

    export default {
        name: 'WatcherReactive',
        setup() {
            const state = reactive({
                first: '',
                last: 'Ganesh',
                options: {
                    role: ''
                }
            });

            // watch(() => {
            //     return { ...state }
            // }, function (new_value, old) {
            //     console.log(new_value, old);
            // }, {
            //     immediate: true
            // });

            watch(() => _.cloneDeep(state.options), function (new_value, old_value) {
                console.log(new_value, old_value);
            }, {
                deep: true
            });


            return {
                ...toRefs(state),
            }
        }
    }
</script>

<style scoped>

</style>