<template>
    <div>
        <input
            type="text"
            class="custom-input"
            :value="modelValue"
            @input="$emit('update:modelValue', $event.target.value)"
        />
    </div>
</template>

<script>
    export default {
        name: 'CustomInput',
        props: {
            modelValue: String,
        }
    }
</script>

<style scoped>
.custom-input {
    border: none;
    border-bottom: 1px solid #ccc;
}
</style>