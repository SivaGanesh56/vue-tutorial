<template>
  <h3 v-if="num === 0">Num is Zero</h3>
  <h3 v-else-if="num < 0">Num is Negative</h3>
  <h3 v-else-if="num > 0">Num is Positive</h3>
  <h3 v-else>Num is Not Number</h3>

   <!-- template helps to wrap content without additional div -->
  <template v-if="display">
    <h2>Siva Ganesh</h2>
    <h3>SDE-2</h3>
    <h5>ShareChat</h5>
  </template>

  <!-- diff b/w v-show & v-if is v-show element will present in DOM with display:none -->
  <h2 v-show="showElement">Show Element</h2>

</template>

<script>

export default {
  name: 'ConditionalVue',
  data() {
    return {
        num: 10,
        display: true,
        showElement: true,
    }
  }
}
</script>

<style>

</style>
