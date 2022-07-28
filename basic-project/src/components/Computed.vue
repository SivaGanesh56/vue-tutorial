<template>
    <h3>Name is {{ firstName }} {{ lastName }}</h3>

    <h3>Computed Name is {{ fullName }}</h3>

    <button @click="changeName">Change Name</button>

    <button @click="items.push({ id: 4, title: 'Laptop', price: 400 })">Add Item</button>

    <h3>Total - {{ total }}</h3>

    <h3 v-for="item of filteredProducts" :key="item.id">{{ item.product }} {{ item.price }}</h3>


    <hr />

</template>

<script>

export default {
    name: 'ComputedVue',
    data() {
        return {
            firstName: 'Siva',
            lastName: 'Ganesh',
            items: [
                {
                    id: 1,
                    title: 'TV',
                    price: 100
                },
                {
                    id: 2,
                    title: 'Mobile',
                    price: 200
                },
                {
                    id: 3,
                    title: 'Fridge',
                    price: 300
                }
            ]
        }
    },
    methods: {
        changeName() {
            this.fullName = 'MS Dhoni'
        }
    },
    computed: {
        fullName: {
            get() {
                return this.firstName + this.lastName;
            },
            set(value) {
                const names = value.split(' ');
                this.firstName = names[0];
                this.lastName = names[1];
            }
            
        },
        total() {
            return this.items.reduce((acc, curr) => acc + curr.price, 0);
        },
        filteredProducts() {
            return this.items.filter(item => item.price > 100);
        },
    }
}
</script>

<style>
</style>
