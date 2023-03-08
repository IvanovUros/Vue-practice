<template>
  <div>
    <CardTest></CardTest>
    <CardTest>Card Content</CardTest>
    <CardTest>
      <h2>Card Content</h2>
    </CardTest>
    <CardTest> 
      <img src="https://picsum.photos/200">
    </CardTest>

    <CardTest>
      <template v-slot:header> 
        <h3>Header</h3>
      </template>
      <template v-slot:default> 
        <img src="https://picsum.photos/200">
      </template>
      <template v-slot:footer> 
        <button>View Details</button>
      </template>
    </CardTest>

    <NameList>
      <template v-slot:default="slotProps">
        {{ slotProps.firstName }} {{ slotProps.lastName }}
      </template>
    </NameList>
    <NameList>
      <template v-slot:default="slotProps">
        {{ slotProps.lastName }} {{ slotProps.firstName }}
      </template>
    </NameList>
    <NameList>
      <template v-slot:default="slotProps">
        {{ slotProps.firstName }}
      </template>
    </NameList>
  </div>

</template>

<script>
import CardTest from './components/CardTest.vue'
import NameList from './components/NameList.vue'

export default {
  name: 'App',
  components: {
    CardTest,
    NameList,
  },
  data() {
    return {

    }
  }
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
