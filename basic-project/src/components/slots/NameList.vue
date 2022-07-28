<template>
    <div>
        <h3 v-for="name of names" :key="name.first">
        <slot :first="name.first" :last="name.last"></slot>
        </h3>
    </div>
</template>

<script>
export default {
    name: 'NameList',
    data() {
        return {
            names: [
                { first: 'Siva', last: 'Ganesh' },
                { first: 'Robin', last: 'Matt' },
                { first: 'MS', last: 'Dhoni' }
            ]
        }
    }
}
</script>

<style scoped>
</style>