<template>
    <h1>Events in VueJS</h1>
    <h2>Current Count is : {{ count }}</h2>
    <button v-on:click="test()" type="button">Click me</button>
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