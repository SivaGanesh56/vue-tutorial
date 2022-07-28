<template>
    <h3 v-for="(name, idx) of names" :key="name">{{ idx + 1 }} {{ name }}</h3>
    <hr />
    <h3 v-for="name of fullNames" :key="name.first">{{ name.first }} {{ name.last }}</h3>

    <hr />
    <div v-for="actor of actors" :key="actor.name">
        <h1>{{ actor.name }}</h1>
        <h3 v-for="movie of actor.movies" :key="movie">{{ movie }}</h3>
    </div>

    <hr />

    <h2 v-for="(value, key, idx) of info" :key="value">{{ idx + 1 }}. {{ key }} : {{ value }}</h2>

    <hr />

    <template v-for="(name, idx) of names" :key="name">
        <h3 v-if="idx < 2">{{ name }}</h3>

    </template>

    <hr />

    <h3>{{ 2 + 3 + 5 }}</h3>
    <h3>{{ sum(2,4,6) }}</h3>
    <h3>{{ baseMultiply(baseValue) }}</h3>

    <hr />

</template>

<script>

export default {
    name: 'ListVue',
    data() {
        return {
            names: ['Siva', 'Ganesh', 'Manyam'],
            fullNames: [
                { first: 'Siva', last: 'Ganesh' },
                { first: 'Robin', last: 'Matt' },
                { first: 'MS', last: 'Dhoni' }
            ],
            actors: [
                {
                    name: 'Prabhas',
                    movies: ['Baahubali', 'Billa']
                },
                {
                    name: 'Tom Curis',
                    movies: ['Mission Impossible', 'Edge of tomorrow']
                }
            ],
            info: {
                name: 'Siva Ganesh',
                role: 'SDE-2',
                location: 'Bangalore'
            },
            baseProduct: 5,
            baseValue: 2,
        }
    },
    methods: {
        sum (a,b,c) {
            return a + b + c;
        },
        baseMultiply(num) {
            return num * this.baseProduct;
        }
    }
}
</script>

<style>
</style>