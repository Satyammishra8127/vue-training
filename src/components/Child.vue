<template>
   <div>
    <h1  :class="{green:colorfull}">
       Child components
    </h1>
    <button v-on:click="colorfull=!colorfull">Apply Style</button>
    <h2>{{ name }}</h2>
    <h3 v-html="tag"></h3>
    <h3 v-html="name1"></h3>
    <h4 v-html="eamil1"></h4>
</div>
</template>

<script>
export default{
    name:'ChildPage',
    props:{
        name:String,
    },
    data(){
        return{
            tag:"<h1>vue-training</h1>",
            name1:"<h2>vue-training</h2>",
            email1:"<h2>parivesh@test.com</h2>",
            colorfull:true
        }
       
    }
}
</script>
<style scoped>
.green{
    background-color:orange;
    width: 200px;
   padding: 10px;


}
</style>
