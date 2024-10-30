<template>
    <h1>Conditional Statements in Vue JS</h1>
    <h2 v-if="show">show</h2>
    <h2 v-else>dont show</h2>
</template>

<style scoped>
   
</style>

<script>
    export default {
        name : 'HelloComponent',
        data(){
            return {
                show : true
            }
        }
    }
</script>