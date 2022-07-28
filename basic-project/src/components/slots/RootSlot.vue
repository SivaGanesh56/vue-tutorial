<template>
    <div>
        <Card></Card>
        <Card>
            <h2>My Title</h2>
        </Card>
        <Card>
            <p>My Paragraph</p>
        </Card>

        <hr />

        <Card>
            <template v-slot:header>
                <h2>Title</h2>
            </template>

            <template v-slot:default>
                <div>
                    <h4>Content comes here</h4>
                </div>
            </template>

            <template v-slot:footer>
                <button>Action buttons</button>
            </template>

        </Card>

        <hr />


        <NameList>
            <template v-slot:default="slotProps">
                <h3>{{ slotProps.first }} {{ slotProps.last }}</h3>
            </template>
        </NameList>

        <NameList>
            <template v-slot:default="slotProps">
                <h3>{{ slotProps.first }}, {{ slotProps.last }}</h3>
            </template>
        </NameList>

        <NameList>
            <template v-slot:default="slotProps">
                <h3>{{ slotProps.first }}</h3>
            </template>
        </NameList>

    </div>
</template>

<script>
import Card from './Card.vue';
import NameList from './NameList.vue';
    export default {
    name: "RootSlot",
    components: { Card, NameList }
}
</script>

<style scoped>

</style>