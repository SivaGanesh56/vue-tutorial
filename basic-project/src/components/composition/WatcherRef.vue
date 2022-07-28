<template>
    <div>
        <input type="text" placeholder="Normal Watch" v-model="name"/>

        <input type="text" placeholder="Ref Watch" v-model="firstName"/>

        <input type="text" placeholder="Ref Watch" v-model="lastName"/>
    </div>
</template>

<script>
import { ref, watch } from 'vue';
    export default {
        name: 'WacherRef',
        data() {
            return {
                name: ''
            }
        },
        setup() {
            const firstName = ref('');
            const lastName = ref('Ganesh');
            
            // watch(firstName, (oldValue, newValue) => {
            //     console.log("oldValue", oldValue);
            //     console.log("newValue", newValue);
            //     console.log('-------');
            // });

            // watch(lastName, (oldValue, newValue) => {
            //     console.log("oldValue", oldValue);
            //     console.log("newValue", newValue);
            //     console.log('-------');
            // }, {
            //     immediate: true
            // });
            

            watch([firstName, lastName], (oldValues, newValues) => {
                console.log("oldValue", oldValues);
                console.log("newValue", newValues);
                console.log('-------');
            }, {
                immediate: true
            });

            return {
                firstName,
                lastName,
            }
        },
        watch: {
            name(oldValue, newValue) {
                console.log("oldValue", oldValue);
                console.log("newValue", newValue);
                console.log('-------');
            }
        }
    }
</script>

<style scoped>

</style>