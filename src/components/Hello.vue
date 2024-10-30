<template>
    <h1>Two Way Binding in VueJS</h1>
    <h2>{{ count }}</h2>
    <input type="text" v-model="count" placeholder="Enter value">
</template>

<style scoped>
   
</style>

<script>
    export default {
        name : 'HelloComponent',
        data(){
            return{
                count : ''
            }
        }
    }
</script>