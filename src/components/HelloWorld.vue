<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    {{str}}
    <button @click="btn">点击</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return{
      name:'jeck'
    }
  },
  props: {
    msg: String,
    // str:'test'
  },
  methods:{
    btn(){
      this.$emit('change',this.name)
    }
  },
  inject:['str']
}
</script>

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
