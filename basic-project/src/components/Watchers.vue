<template>
    <h3>Volume Level - (0-20)</h3>

    <h4>Current Level - {{ volume }}</h4>

    <div>
        <button @click="volume += 2">Inc</button>
        <button @click="volume -= 2">Dec</button>
    </div>

    <input type="text" v-model="movie" />

    <input type="text" v-model="movieInfo.title" />
    <input type="text" v-model="movieInfo.actor" />

    <hr />

</template>

<script>

export default {
    name: 'ListVue',
    data() {
        return {
            volume: 0,
            movie: 'Baahubali',
            movieInfo: {
                title: '',
                actor: ''
            }
        }
    },
    methods: {
    },
    watch: {
        volume(newValue, oldValue) {
            if (newValue > oldValue && newValue == 16) {
                alert('high volume increase alert');
            }
        },
        movie: {
            handler(newValue) {
                console.log('Calling API call with movie name - ', newValue);
            },
            immediate: true, // calls when page loads
        },
        movieInfo: {
            handler(newValue) {
                console.log('Receievd new value', newValue);
            },
            deep: true,
        }
    }
}
</script>

<style>
</style>