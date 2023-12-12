<template>
<div>
    <h1 >Blog</h1>
    <button v-on:click="getData()">click me</button>
    <button v-on:click="getConsole()">click me</button>
    <h2>{{count}}</h2>
</div>
</template>

<script>
export default {
    name: "HomePage",
    data(){
        return{
            count:0
        }
    },
    methods:{
        getData() {
             this.count=this.count+1
        },
        getConsole() {
             this.count=this.count-1
        }

    }
}
</script>

<style>
</style>
