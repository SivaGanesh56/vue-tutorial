<template>
    <div>
        <input type="text" placeholder="first" v-model="first"/>
        <input type="text" placeholder="last" v-model="last"/>

        <PropsGreet :first="first" :last="last" @call="alertUser"/>
    </div>
</template>

<script>
import { ref } from 'vue'
import PropsGreet from './PropsGreet.vue';

    export default {
    name: "Props",
    setup() {
        const first = ref("");
        const last = ref("");

        function alertUser(value) {
            alert(value);
        }

        return {
            first,
            last,
            alertUser
        };
    },
    components: { PropsGreet }
}
</script>

<style scoped>

</style>