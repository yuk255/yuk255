<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App" @change="btn1">
      插槽传递内容
    </HelloWorld>

  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  data(){
    return{
      str:"abc"
    }
  },
  components: {
    HelloWorld
  },
  methods:{
    btn1(val){
      console.log(val);
    }
  },
  provide(){
    return{
      str:this.str
    }
  }
}
</script>
