<template>
    <h3>
        Hello {{ name }} aka {{ alias }}
    </h3>
</template>

<script>
export default {
    name: 'GreetVue',
    props: ['name', 'alias']
}
</script>

<style scoped>
</style>