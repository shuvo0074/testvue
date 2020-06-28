<template>
  <div class="hello"
  :style="[appStyle,appStyle2]"  
  >
  <!--    :style="{backgroundColor: "#42b983"}"  
  or --   style="backgroundColor: #42b983" This is inline style, without binding, you can't use variable here -->

    <h1
    class="msgTxt"
    :class="[msg==desiredMessage?'desiredMsgTxt':'']"
    @mouseover="dim"
    >{{ msg }}</h1>
    <!-- if props.msg is same as data.desiredMessage class desiredMsgTxt is applied 
    condition can be applied like this too     :class="{desiredMsgTxt:msg==desiredMessage}"
    -->
    <h1>{{messages}} </h1>
    <div :key="item.id" v-for="item in lists" >
      <h3>{{item.title}} </h3>
      <ListItem :naame="item" />
    </div>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script>
  import ListItem  from "./LisItem.vue";

export default {
  name: 'HelloWorld',
  components: {
    ListItem
    },
  props:
  ["lists","msg"],
  // {
  //   msg: String,
  //   lists: ["lists"]
  // },
  data(){
    return{
      messages: 'msg',
      colorBack: '#42b983',
      appStyle:{
        backgroundColor: "#42b983"
      },
      appStyle2:{
          // color: "blueviolet"
      },
      desiredMessage:"Welcome"
      // firstText: $props
    }
    
  },
  methods: {
    dim (){
      console.log(this.colorBack,"somreoenr")
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
.msgTxt {
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-weight: bolder;
  color: azure;
}
.desiredMsgTxt{
  text-decoration:underline;
}
a {
  color:brown;
}
</style>
