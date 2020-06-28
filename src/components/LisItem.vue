<template>
    <div>
        <p
        id= "p1"
        class="msgTxt"
        @mouseover="dim"
        >
        <!--         :class="{msgTxt:true}"  you have to bind class if there is a condition -->
            {{title}}
        </p>
    </div>
</template>
<script>
export default {
    name: "ListItem",
    props: ["naame"],
    computed:{
        title(){
            return 'we'+ ' '+"like "+this.naame.title
            // That;s how you use props
            }
    },
    methods: {
        dim(){
            console.log("props.naame",this.naame)
            // this.naame.settitle("hudamisa")
        }
    },
    
}
</script>
<style scoped>
#p1{
    font-size: 40;
}
.msgTxt {
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  color: azure;
  font-weight: bolder;
}
</style>