<template>
    <h1>Events in VueJS</h1>
    <h2>Current Count is : {{ count }}</h2>
    <button v-on:dblclick="test()" type="button">Double Click me</button>
    <br> <br>
    <button v-on:mousemove="test()" type="button">Hover on me</button>
</template>

<style scoped>
   
</style>

<script>
    export default {
        name : 'HelloComponent',
        data(){
            return {
                count : 0,
            }
        },
        methods : {
            test(){
                this.count+=1;
            }
        }
    }
</script>