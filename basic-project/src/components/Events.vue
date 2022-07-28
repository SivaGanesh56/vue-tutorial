<template>
    <h1>Hello {{ name }}</h1>
    <div>
        <button v-on:click="changeName">Change Name</button>
    </div>

    <hr />

    <h2>Count: {{ count }}</h2>
    <div>
        <button @click="count = count + 1">Increment</button>
        <button @click="count = count - 1">Decrement</button>
        <button @click="inc(5, $event)">Increment By 5</button>
        <button @click="dec(3)">Decrement By 3</button>

        <button @click="changeName($event), inc(1, $event)">Increment & Change Name</button>
    </div>


    <hr />

</template>

<script>

export default {
    name: 'EventsVue',
    data() {
        return {
            name: 'Siva',
            count: 0
        }
    },
    methods: {
        changeName(event) {
            console.log(event);
            this.name = 'Baahubali'
        },
        inc(num, event) {
            console.log(event);
            this.count += num;
        },
        dec(num) {
            this.count -= num;
        }
    }
}
</script>

<style>
</style>
