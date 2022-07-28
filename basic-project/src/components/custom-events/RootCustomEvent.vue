<template>
    <div>
        <button @click="open = true">open popup</button>

        <Popup v-show="open" @close="closePopup"/>

        <CustomInput v-model="name"/>
 
        
    </div>
</template>

<script>
    import Popup from './ChildComponent.vue'
import CustomInput from './customInput.vue';
    export default {
        name: 'RootCustomEvent',
        data() {
            return {
                open: false,
                name: ''
            }
        },
        components: {
    Popup,
    CustomInput
},
        methods: {
            closePopup(name) {
                this.open = false;
                console.log(name);
            }
        }
    }
</script>

<style scoped>

</style>