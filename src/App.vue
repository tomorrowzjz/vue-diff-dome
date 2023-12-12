<template>
  <div id="app">
    <div v-if="isShow">testshow</div>
    <div>Vue logo</div>
    <div>
      <HelloWorld msg="HelloWorld" @testDiff="testDiff"/>
    </div>
    <div v-if="isShow">btn</div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    return {
      isShow:false
    }
  },
  components: {
    HelloWorld
  },
  methods:{
    testDiff(){
      this.isShow = !this.isShow
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
