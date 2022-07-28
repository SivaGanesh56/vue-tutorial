<template>
  <!-- <Basic></Basic> -->
  <!-- <ConditionalVue></ConditionalVue> -->
  <!-- <ListVue></ListVue> -->
  <!-- <EventsVue></EventsVue> -->
  <!-- <FormsVue></FormsVue> -->
  <!-- <ComputedVue></ComputedVue> -->
  <!-- <WatchersVue></WatchersVue> -->
  <!-- <RootComponentVue></RootComponentVue> -->
  <!-- <ProvideRootVue></ProvideRootVue> -->
  <!-- <RootCustomEventVue /> -->
  <!-- <RootSlotVue /> -->
  <!-- <div>
    <h4>App Component Styles</h4>
  <ChildStylesVue></ChildStylesVue>
  </div> -->

  <!-- <root-dynamic-component /> -->

  <!-- <RootHttp /> -->

  <!-- <RootRef /> -->

  <!-- <RootMixin /> -->

  <RootComposition />
</template>

<script>
// import Basic from './components/Basic.vue'
// import ConditionalVue from './components/Conditional.vue'
// import ListVue from './components/List.vue'
// import EventsVue from './components/Events.vue';
// import FormsVue from './components/Forms.vue'
// import ComputedVue from './components/Computed.vue'
// import WatchersVue from './components/Watchers.vue';
// import RootComponentVue from './components/subcomponents/RootComponent.vue';
// import ProvideRootVue from './components/provide-inject/ProvideRoot.vue';
// import RootCustomEventVue from './components/custom-events/RootCustomEvent.vue'
// import RootSlotVue from './components/slots/RootSlot.vue';
// import ChildStylesVue from './components/childStyles.vue'
// import RootDynamicComponent from './components/dynamic-components/RootDynamicComponent.vue'
// import RootHttp from './components/http/RootHttp.vue'
// import RootRef from './components/refs/RootRef.vue'
// import RootMixin from './components/mixins/RootMixin.vue'
import RootComposition from './components/composition/RootComposition.vue'

export default {
  name: 'App',
  components: {
    // Basic,
    // ConditionalVue,
    // ListVue,
    // EventsVue,
    // FormsVue,
    // ComputedVue,
    // WatchersVue,
    // RootComponentVue,
    // ProvideRootVue,
    // RootCustomEventVue,
    // RootSlotVue,
    // ChildStylesVue,
    // RootDynamicComponent,
    // RootHttp,
    // RootRef,
    // RootMixin,
    RootComposition
}
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

/* h4 {
  color: red
} */
</style>
