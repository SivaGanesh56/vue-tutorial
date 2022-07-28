<template>
    <div>
        <form @submit.prevent="onSubmit">
            <input type="text" placeholder="userId" v-model="formData.userId" />
            <input type="text" placeholder="title" v-model="formData.title" />
            <input type="text" placeholder="body" v-model="formData.body" />
            <button>Post</button>
        </form>
    </div>
</template>

<script>
import axios from 'axios';
export default {
    name: 'CreatePost',
    data() {
        return {
            formData: {
                userId: '',
                title: '',
                body: ''
            }
        }
    },
    methods: {
        onSubmit: async function () {
            try {
                const response = await axios.post('https://jsonplaceholder.typicode.com/posts', {
                    data: this.formData
                });
                console.log(response);
            } catch (error) {
                console.log(error);
            }
        }
    }
}
</script>

<style scoped>
</style>