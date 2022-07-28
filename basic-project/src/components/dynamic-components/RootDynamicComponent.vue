<template>
    <div class="tabs">
        <div class="tab-btn-group">
            <button @click="activeTab = 'TabA'">TabA</button>
            <button @click="activeTab = 'TabB'">TabB</button>
            <button @click="activeTab = 'TabC'">TabC</button>
        </div>

        <keep-alive>
            <component :is="activeTab" />
        </keep-alive>

        <teleport to="#portal-root">
            <Modal></Modal>
        </teleport>
       
    </div>
</template>

<script>
import TabA from './TabA.vue';
import TabB from './TabB.vue';
import TabC from './TabC.vue';
import Modal from './Modal.vue';
export default {
    name: "RootDynamicComponent",
    components: { TabA, TabB, TabC, Modal },
    data() {
        return {
            activeTab: 'TabA'
        }
    }
}
</script>

<style scoped>
.tabs {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.tab-btn-group {
    display: flex;
}
</style>