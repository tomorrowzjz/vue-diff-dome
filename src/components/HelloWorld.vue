<template>
  <div class="hello">
    <h1 @click="testDiff">{{ msg }}</h1>
    <div>{{test}}</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return {
      test: this.msg
    }
  },
  mounted(){
    console.log("HelloWorld-mounted")
  },
  methods:{
    testDiff(){
      this.$emit('testDiff')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
