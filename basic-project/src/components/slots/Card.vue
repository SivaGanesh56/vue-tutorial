<template>
    <div class="card">
        <div class="card-header">
            <slot name="header"></slot>
        </div>

        <div class="card-content">
            <slot>Default Content</slot>
        </div>

        <div class="card-footer">
            <slot name="footer"></slot>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Card'
    }
</script>

<style scoped>
.card {
    border: 1px solid #ccc;
    padding: 20px;
    width: fit-content;
}
</style>