<template>
    <div>
        <h3>This is Popup</h3>
        <input type="text" v-model="name"/>
        <button @click="$emit('close', name)">Close Popup</button>
    </div>
</template>

<script>
    export default {
        name: 'ChildPopUpComponent',
        data() {
            return {
                name: '',
            }
        },
        emits: {
            close: (name) => {
                if (!name) return false;
                return true;
            }
        }
    }
</script>

<style scoped>

</style>