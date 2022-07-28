<template>
    <div>
        <h3>Original - {{ o_name }}</h3>

        <h3>Composition - {{ c_name }}</h3>

        <h3>{{ greet }}</h3>

        <input v-model="text"/>
    </div>
</template>

<script>
import { ref } from 'vue'

    export default {
        name: 'Data',
        setup() {
            const c_name = ref('Ganesh');

            const text = ref('');

            const greet = `Hello ${c_name.value}`

            return {
                c_name,
                greet,
                text
            }
        },
        data() {
            return {
                o_name: 'Siva'
            }
        }
    }
</script>

<style scoped>

</style>