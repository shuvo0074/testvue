<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld :lists="lists" msg="Welcome"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  data(){
    return{
      lists: [
        {
          id:1,
          title: "one"
        },
        {
          id:2,
          title: 'two'
        }
      ]
    }
  }
}
</script>

<style>
.msgTxt {
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  color: brown;
  font-weight: bolder;
}

</style>