<template>
    <div>
        <input type="text" ref="myRef"/>
    </div>
</template>

<script>
import { onMounted, ref } from 'vue'

    export default {
        name: 'Refs',
        setup() {
            const myRef = ref(null);

            onMounted(() => {
                myRef.value.focus();
            });

            return {
                myRef,
            }
        }
    }
</script>

<style scoped>

</style>