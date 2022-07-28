<template>
  <h1>Components</h1>

  <GreetVue name="Siva" alias="Baahuali"/>
  <GreetVue name="Ganesh" alias="Billa"/>
  <GreetVue name="Manyam" alias="Batman"/>

  <GreetVue :name="name" :alias="alias"/>

  <hr />

  <ArticleVue id="article" title="My Title" :published="true" :noOfComments="10" />

  <hr />
</template>

<script>

import GreetVue from './Greet.vue';
import ArticleVue from './Article.vue';

export default {
  name: 'RootComponent',
  data() {
    return {
        name: 'Alex',
        alias: 'al'
    }
  },
  components: {
    GreetVue,
    ArticleVue,
  }
}
</script>

<style>
</style>
