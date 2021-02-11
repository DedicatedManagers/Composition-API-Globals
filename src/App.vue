<template>
  Below are two components that both pull a reactive variable from a shared global.js file.<br>
  <hr>
  <ComponentOne />
  <hr>
  <ComponentTwo />
  <hr>
  <ComponentThree />
</template>

<script>
import ComponentOne from './components/ComponentOne.vue'
import ComponentTwo from './components/ComponentTwo.vue'
import ComponentThree from './components/ComponentThree.vue'

export default {
  name: 'App',
  components: {
    ComponentOne,
    ComponentTwo,
    ComponentThree,
  }
}
</script>

<style>
</style>
