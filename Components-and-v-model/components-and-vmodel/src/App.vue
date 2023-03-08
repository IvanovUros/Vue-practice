<template>
<div>
  <InputTest v-model="name"/>
</div>
</template>

<script>
import InputTest from './components/InputTest.vue'
export default {
  name: 'App',
  components: {
    InputTest,
  },
  data() {
    return {
      name: ''
    }
  },
  methods: {},
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
